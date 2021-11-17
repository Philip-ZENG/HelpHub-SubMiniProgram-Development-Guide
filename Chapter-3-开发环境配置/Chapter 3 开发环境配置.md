# Chapter 3 开发环境配置

最后更新日期：2021年11月17日

作者：曾焯儒、金一鑫



在这一章节我们将介绍小程序开发环境的配置方法。在跟随本章节指引完成操作之后，你将能够成功编译出HelpHub+小程序。



## 小程序编译环境配置

- Node.js安装

  - 介绍

    Node.js是一个在本地模拟网页运行的“虚拟服务器”。通过Node.js提供的功能，我们可以将本地的网页设计文件、小程序文件进行编译，并且在浏览器、小程序开发工具中查看其呈现效果。

  - nodejs 环境要求

    - [nodejs >= 11.10.1](https://nodejs.org/dist/v11.15.0/) 注意：nodejs v12 版本有bug
    - 笔者下载的版本是：v14.18.0 -x64

  - 去官网下载
    
    - 可以使用yarn的中文网站或英文网站 ，都可以直接下载稳定版v14.18.0的msi文件
    
    - 英文网：https://nodejs.org/en/
    - 中文网：http://nodejs.cn/

- Yarn 安装

  - 介绍
    - 可以把Yarn看作是一个用于下载各种包的下载和管理中心，类似python的pip，和Node.js的npm是几乎同等功能的
  - 版本要求
    - [yarn >= 1.22.4](https://classic.yarnpkg.com/en/docs/install)
    - 笔者安装的是v1.22.15

- Taro安装

  - 介绍

    - Taro是基于Vue或者React（JavaScript的库）搭建的一个更加上层的框架，它提供了微信小程序搭建所需的一些框架、组件、工具，通过Taro，我们可以便捷地实现小程序的搭建。

  - Taro环境安装指令参考

    - 开发者使用了特定的Tarojs的版本 `2.2.1`，请在terminal/shell中依次运行下列指令

      ```shell
      yarn add -D @tarojs/cli@2.2.1
      
      yarn add -D @tarojs/mini-runner@2.2.1
      
      yarn add global mirror-config-china 
      ```

    - 注意事项

      - 如果在源文件的根目录文件夹下运行失败，可以尝试在其他位置运行指令，如：在desktop打开terminal运行

  - 其他Taro下载参考：请注意下载 `2.2.1` 版本

    - 官方文档： 

      - https://taro-docs.jd.com/taro/docs/GETTING-STARTED#cli-%E5%B7%A5%E5%85%B7%E5%AE%89%E8%A3%85 

      - 请根据官方文档指引完成下载
    - 技术博客：https://www.cnblogs.com/cczlovexw/p/13808842.html
      - 其中有一个Hello World的DEMO教学，可以试着做一下

  - 可能存在的问题

    - 对于Terminal“无法识别taro"问题，需要配置环境变量：https://blog.csdn.net/qq_34209233/article/details/105262687?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-2.no_search_link&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7Edefault-2.no_search_link

- Git ssh密钥配置

  - 介绍
    - 密钥是一种在本地电脑于云端之间建立安全的数据传输渠道的方式。
  - 密钥配置可以参考链接 https://www.cnblogs.com/yuqiliu/p/12551258.html
  - 对于过程中可能遇到的问题，可以参考： https://www.codenong.com/13363553/
  - 注意事项
    - 不要设置密钥密码。

    - 密钥必须使用一次(git clone ssh://XXXXX 拉一个项目的代码)，不然yarn会安装失败。
  - Remark: 考虑到我们没有权限从微盟的代码库里pull东西，感觉其实不做这一步也没什么影响

- 依赖安装 (Dependencies)

  ```
  yarn
  ```

  - 在源码根目录下运行时，可能会遇到如下问题

    ```shell
    error Command failed.
    Exit code: 128
    Command: git
    Arguments: ls-remote --tags --heads git@codeup.aliyun.com:5f855dfb1858a17210466fd0/r_d_center/eslint-config-wmeimob.git
    Directory: C:\Users\89254\Desktop\Sub-MiniProgram\helphub-sub-mini-program
    Output:
    Host key verification failed.
    fatal: Could not read from remote repository.
    
    Please make sure you have the correct access rights
    and the repository exists.
    info Visit https://yarnpkg.com/en/docs/cli/install for documentation about this command.
    ```

    - 出问题的文件是：package.json

    - 出问题的代码是第86行

      ```shell
      "eslint-config-wmeimob": "ssh://git@codeup.aliyun.com:5f855dfb1858a17210466fd0/r_d_center/eslint-config-wmeimob.git"，
      ```

    - 这个应该是微盟自己开发的时候储存在”阿里云效代码管理“  codeup.aliyun.com 的一个内部的 eslint debug设置，我们没有权限下载依赖。

    - 删除这一行之后，能供成功完成所有其他的路径下载，暂时（没有Debug的时候）来看删掉好像也没什么影响。

  - `yarn` 成功执行后，将node_modules-cover 里面的文件复制到 node_modules下

- 调试

  在源码根目录下运行

  ```
  yarn dev
  ```

- 打包

  在源码根目录下运行

  ```
  yarn build
  ```

- 在微信开发者工具运行源代码

  - 编译完成后，在微信开发者工具界面打开工程
  - 打开工程后将可以呈现出UI界面
  - Remark: 因为没有链接到云端数据库，也没有配置网络所以在点击”登录”按钮时，会显示“网络请求失败”
  - 至此，如果能成功看到UI界面，则说明环境配置基本成功了



## VSCode配置

- 开发方使用VSCode进行代码开发及调试

- 推荐的vscode插件

  - `ESLint` 
  - `CSS Modules` 
  - `Document This`

- vscode配置

  默认vscdoe的eslint不会检测tsx文件，不会自动修复，需要手动开启

  ```
  "eslint.autoFixOnSave": true,
      "eslint.validate": [
          "javascript",
          "javascriptreact",
          {
              "language": "typescript",
              "autoFix": true
          },
          {
              "language": "typescriptreact",
              "autoFix": true
          }
      ],
  ```

