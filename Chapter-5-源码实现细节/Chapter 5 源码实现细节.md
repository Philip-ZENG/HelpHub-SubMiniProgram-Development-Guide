# Chapter 5 源码实现细节

最后更新日期：2021年10月25日

作者：曾焯儒



这一章节，我们将学习源码的具体实现细节。我们将对源码核心文件的函数功能、接口以及实现原理进行详细的分析与介绍。在完成本章节的学习后，你将掌握修改源码的基本知识技能并且熟悉小程序各功能的实现原理，这将为你在下一阶段的源码修改工作打下基础。



## 源代码中用到的相关技术

参考资料链接如下

- JavaScript教程
  - <https://wangdoc.com/javascript/> 
- ES6教程
  - <http://es6.ruanyifeng.com/> 
- 应该是CSS教程（但好像打不开）
  - <http://css.cuishifeng.cn/position.html> 
  - JS,CSS,HTML教程也可参考HelpHub-Web-Development-Guide的Chapter 2
    - https://github.com/Philip-ZENG/HelpHub-SubMiniProgram-Development-Guide.git
- Taro官方文档
  - <https://nervjs.github.io/taro/docs/README.html> 
- Taro UI官方文档
  - <https://taro-ui.aotu.io/#/docs/introduction> 
- React中文官方文档
  - <https://react.docschina.org/> 
- TypeScript中文官网
  - <https://www.tslang.cn/> 
  - TypeScript在JavaScript的基础上提供了更多代码样式和调试工具



## 学习进程

- JavaScript Brief Review:
  -  https://developer.mozilla.org/en-US/docs/Web/JavaScript/A_re-introduction_to_JavaScript

- Learn by going through a document: 
  - https://reactjs.org/docs/getting-started.html

- Learn by going through a tutorial: 
  - https://reactjs.org/tutorial/tutorial.html
  - Tips:
    - Do not create your react project on desktop, there would be `babel-eslint`  version problems
      - The writer create it on `D:\`
    - use `yarn start` to start a development mode and see the effects in browser

- Taro tutorial: 
  - https://docs.taro.zone/docs/guide



## 前端UI组件

[前端组件列表](https://git.f.wmeimob.com/Frontend/front-end-catalog/src/master/project.md)

- 我们无法进入该网页



