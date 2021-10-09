# Chapter 4 源码架构分析

最后更新日期：2021年10月4日

作者：曾焯儒



这一部分，我们将对源代码的架构以进行分析，主要关注Taro的项目架构以及Source部分的代码功能。在完成本章节的学习后，你将能够理解源代码各个部分的作用并且快速定位实现某一功能的代码的位置。



## Taro框架

参考资料：

- Taro目录结构官方文档：https://taro-docs.jd.com/taro/docs/folder
- Taro使用教程：https://www.cnblogs.com/cczlovexw/p/13808842.html



Taro是由京东凹凸实验室推出的框架，目的就是解决多端混乱的局面，也是当下比较新兴的一个框架。我们可以按照一种模式一种代码进行开发，开发完成后，项目就有了在任何终端显示的能力。基于笔者的理解，Taro应该是基于Vue或React等框架，专门为搭建国内各类软件平台上的小程序建立的，更高层的框架。

- Remark: Taro使用的技术栈是React，HelpHub的网页开发项目使用的技术栈是Vue，如果你先前有接触过HelpHub的网页项目，对于Taro的学习将会让你产生熟悉的感觉。

- 学习这个前端框架，你需要一些前置知识：
  - HTML、CSS，JavaScript这三个是基础知识，最起码要了解，能作出简单的静态页面
    - HelpHub-Web-Development-Guide 的 Chapter 2 有关于HTML,CSS,JavaScript的入门教学
    - 链接: https://github.com/Philip-ZENG/HelpHub-Web-Development-Guide
  - 理解MVVM框架，如果会React框架是最好的
  - 了解ES6相关语法，作为一个当下流行的框架以及2020年的前端开发用ES6让代码规范起来，对项目开发和管理更加的方便

- Taro默认模板的生成

  - 在Terminal运行下列代码，跟随指引选择配置即可。

    ```
    taro init
    ```

  - 运行项目

    - 生成h5网页界面

      ```
      npm run dev:h5
      ```

    - 生成微信小程序

      ```
      npm run dev:weapp
      ```

    - Remark: 使用yarn指令也可以实现同样的效果

  - Remark: 在学习源码架构之前，我们可以先学习一下Taro默认模板的架构，通过对比来了解源码增添了那些内容。

- Taro默认模板目录

  ```
  ├── dist                        编译结果目录
  |
  ├── config                      项目编译配置目录
  |   ├── index.js                默认配置
  |   ├── dev.js                  开发环境配置
  |   └── prod.js                 生产环境配置
  |
  ├── src                         源码目录
  |   ├── pages                   页面文件目录
  |   |   └── index               index 页面目录
  |   |       ├── index.js        index 页面逻辑
  |   |       ├── index.css       index 页面样式
  |   |       └── index.config.js index 页面配置
  |   |
  |   ├── app.js                  项目入口文件
  |   ├── app.css                 项目总通用样式
  |   └── app.config.js           项目入口配置
  |
  ├── project.config.json         微信小程序项目配置 project.config.json
  ├── project.tt.json             字节跳动小程序项目配置 project.config.json
  ├── project.swan.json           百度小程序项目配置 project.swan.json
  ├── project.qq.json             QQ 小程序项目配置 project.config.json
  |
  ├── babel.config.js             Babel 配置
  ├── tsconfig.json               TypeScript 配置
  ├── .eslintrc                   ESLint 配置
  |
  └── package.json
  ```

  

## 小程序源码目录结构

- 微盟提供的目录结构说明

  ```
  config:taro 配置
  dist:打包目录（编译结果目录）【编译自动生成，我们一般不用管】
  doc:文档
  node_modules-cover:node_modules覆盖目录
  node_modules:项目所需的依赖包【工程初始化和依赖安装时生成，我们一般不用管】
  src:开发目录【这个是最重要的源码目录，开发的所有代码都在这个里面】
      components:组件（全局组件，全局方法）
          assets:放置公用静态文件  
          component:组件模板  
          event-emitter:事件  
          request:请求组件  
              index.ts:请求文件  
              listener.ts:token注入  
          taro:taro函数修改  
          utils:公用函数  
      custom-tab-bar：自定义导航
      modules:放置公司做的组件
      pages:页面
          _template:页面模版  用于复制粘贴生成新页面
          template:页面模版  用于了解基本写法
      types:d.ts 补全
      app.less:样式入口  
      app.tsx:js入口  
      config.ts:配置文件  
      globalStore.ts:全局数据
      index.html:html5项目的入口
  tools:工具脚手架
  ```

- 详细的工程目录及说明在本文件夹内的Appendix-4.1中
  - 你可以自行生成项目目录结构
    - 参考：https://www.jianshu.com/p/1440c9b785d5

- 重点关注文件

  - `src\pages`  下的各页面文件

    ```
    |  ├─pages【页面实现】
    |  |   ├─_template【页面模板，用于复制粘贴生成新页面】
    |  |   |     ├─index.module.less【less文件，less是css的延申版本，用于设置界面呈现样式】
    |  |   |     ├─index.tsx【typescript文件，typescript是javascript的延申版本，包含html文件的内容，用于设置页面交互逻辑和呈现内容】
    |  |   |     └store.ts
    |  |   ├─login【登录界面】
    |  |   |   ├─index.module.less
    |  |   |   ├─index.tsx
    |  |   |   ├─store.ts
    |  |   |   ├─images
    |  |   |   |   ├─iconA.png
    |  |   |   |   ├─iconP.png
    |  |   |   |   └logo.png
    |  |   ├─home【主页】
    |  |   |  ├─index.module.less
    |  |   |  ├─index.tsx
    |  |   |  ├─scoll.tsx
    |  |   |  ├─store.ts
    |  |   |  ├─images
    |  |   |  |   ├─icon_classify.png
    |  |   |  |   ├─icon_time.png
    |  |   |  |   ├─icon_user.png
    |  |   |  |   └tabIcon.png
    |  |   ├─cancelList【核销页面】
    |  |   |     ├─index.module.less
    |  |   |     ├─index.tsx
    |  |   |     ├─store.ts
    |  |   |     ├─images
    |  |   |     |   ├─sao_bg.png
    |  |   |     |   └sao_icon.png
    ```

    
