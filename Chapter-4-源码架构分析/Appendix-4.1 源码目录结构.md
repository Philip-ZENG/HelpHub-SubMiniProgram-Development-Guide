Notice: node_modules（项目所需的依赖包）没有显示在该目录中

Sub-MiniProgram\helphub-sub-mini-program
├─.editorconfig
├─.eslintignore
├─.eslintrc.js
├─.gitignore
├─global.d.ts
├─mm-config.js
├─package-lock.json
├─package.json【设置依赖安装步骤需要下载的依赖包】
├─project.config.json【微信小程序项目配置 project.config.json】
├─project.private.config.json
├─README.md
├─tsconfig.json【TypeScript 配置】
├─yarn-error.log
├─yarn.lock
├─tools
|   └.empty
├─src【程序开发源码】
|  ├─app.jsx.map
|  ├─app.less
|  ├─app.tsx
|  ├─config.ts
|  ├─GlobalData.ts
|  ├─globalStore.js.map
|  ├─globalStore.ts
|  ├─index.html
|  ├─lifeCycle.ts
|  ├─types
|  |   └taro.d.ts
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
|  ├─openApiModel
|  |      ├─web-api
|  |      |    └index.ts
|  ├─modules【微盟公司制作的组件】
|  |    ├─@wmeimob
|  |    |    ├─utils
|  |    |    |   ├─package.json
|  |    |    |   ├─src
|  |    |    |   |  ├─web
|  |    |    |   |  |  ├─index.tsx
|  |    |    |   |  |  ├─hooks
|  |    |    |   |  |  |   ├─index.ts
|  |    |    |   |  |  |   ├─use-boolean.ts
|  |    |    |   |  |  |   ├─use-enum.ts
|  |    |    |   |  |  |   └use-list.ts
|  |    |    |   |  ├─taro
|  |    |    |   |  |  └index.tsx
|  |    |    |   |  ├─react-native
|  |    |    |   |  |      ├─classnames.js
|  |    |    |   |  |      ├─classnames.ts
|  |    |    |   |  |      ├─index.js
|  |    |    |   |  |      ├─index.ts
|  |    |    |   |  |      └permission.ts
|  |    |    |   |  ├─other
|  |    |    |   |  |   └index.ts
|  |    |    |   |  ├─high-function
|  |    |    |   |  |       ├─index.js
|  |    |    |   |  |       └index.ts
|  |    |    ├─taro-design
|  |    |    |      ├─package.json
|  |    |    |      ├─src
|  |    |    |      |  ├─components
|  |    |    |      |  |     ├─utils
|  |    |    |      |  |     |   └index.ts
|  |    |    |      |  |     ├─textarea
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    └index.tsx
|  |    |    |      |  |     ├─test
|  |    |    |      |  |     |  └index.tsx
|  |    |    |      |  |     ├─tabs
|  |    |    |      |  |     |  ├─const.ts
|  |    |    |      |  |     |  ├─index.modules.less
|  |    |    |      |  |     |  └index.tsx
|  |    |    |      |  |     ├─tab-bar
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    ├─index.tsx
|  |    |    |      |  |     |    ├─images
|  |    |    |      |  |     |    |   ├─sop-cgdd-hover.png
|  |    |    |      |  |     |    |   └sop-cgdd.png
|  |    |    |      |  |     ├─switch
|  |    |    |      |  |     |   ├─index.modules.less
|  |    |    |      |  |     |   └index.tsx
|  |    |    |      |  |     ├─styles
|  |    |    |      |  |     |   ├─global.less
|  |    |    |      |  |     |   ├─index.less
|  |    |    |      |  |     |   ├─reset.less
|  |    |    |      |  |     |   ├─utils
|  |    |    |      |  |     |   |   └index.less
|  |    |    |      |  |     |   ├─themes
|  |    |    |      |  |     |   |   ├─default.less
|  |    |    |      |  |     |   |   └default.modules.less
|  |    |    |      |  |     |   ├─color
|  |    |    |      |  |     |   |   ├─bezierEasing.less
|  |    |    |      |  |     |   |   ├─colorPalette.less
|  |    |    |      |  |     |   |   ├─colors.less
|  |    |    |      |  |     |   |   └tinyColor.less
|  |    |    |      |  |     ├─stepper
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    └index.tsx
|  |    |    |      |  |     ├─stars
|  |    |    |      |  |     |   ├─const.ts
|  |    |    |      |  |     |   ├─index.modules.less
|  |    |    |      |  |     |   └index.tsx
|  |    |    |      |  |     ├─sku-list
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    └index.tsx
|  |    |    |      |  |     ├─pull-to-refresh
|  |    |    |      |  |     |        ├─const.tsx
|  |    |    |      |  |     |        ├─index.modules.less
|  |    |    |      |  |     |        └index.tsx
|  |    |    |      |  |     ├─progress
|  |    |    |      |  |     |    ├─const.ts
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    └index.tsx
|  |    |    |      |  |     ├─popover
|  |    |    |      |  |     |    ├─const.ts
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    └index.tsx
|  |    |    |      |  |     ├─picker
|  |    |    |      |  |     |   ├─index.modules.less
|  |    |    |      |  |     |   ├─index.tsx
|  |    |    |      |  |     |   └view.tsx
|  |    |    |      |  |     ├─navigation
|  |    |    |      |  |     |     ├─const.tsx
|  |    |    |      |  |     |     ├─index.modules.less
|  |    |    |      |  |     |     └index.tsx
|  |    |    |      |  |     ├─modal
|  |    |    |      |  |     |   ├─alert.tsx
|  |    |    |      |  |     |   ├─const.ts
|  |    |    |      |  |     |   ├─index.modules.less
|  |    |    |      |  |     |   ├─index.tsx
|  |    |    |      |  |     |   ├─popup.tsx
|  |    |    |      |  |     |   ├─title.tsx
|  |    |    |      |  |     |   └toast.tsx
|  |    |    |      |  |     ├─menu
|  |    |    |      |  |     |  ├─index.modules.less
|  |    |    |      |  |     |  └index.tsx
|  |    |    |      |  |     ├─loading
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    ├─index.tsx
|  |    |    |      |  |     |    └types.ts
|  |    |    |      |  |     ├─item
|  |    |    |      |  |     |  ├─index.modules.less
|  |    |    |      |  |     |  ├─index.tsx
|  |    |    |      |  |     |  ├─input.modules.less
|  |    |    |      |  |     |  ├─input.tsx
|  |    |    |      |  |     |  ├─leftIconfont.tsx
|  |    |    |      |  |     |  ├─must.modules.less
|  |    |    |      |  |     |  ├─must.tsx
|  |    |    |      |  |     |  ├─placeholderText.tsx
|  |    |    |      |  |     |  ├─rightIconfont.tsx
|  |    |    |      |  |     |  ├─rightText.tsx
|  |    |    |      |  |     |  └text.tsx
|  |    |    |      |  |     ├─input-search
|  |    |    |      |  |     |      ├─const.ts
|  |    |    |      |  |     |      ├─index.modules.less
|  |    |    |      |  |     |      └index.tsx
|  |    |    |      |  |     ├─index-bar
|  |    |    |      |  |     |     ├─index.modules.less
|  |    |    |      |  |     |     └index.tsx
|  |    |    |      |  |     ├─image-picker
|  |    |    |      |  |     |      ├─index.modules.less
|  |    |    |      |  |     |      └index.tsx
|  |    |    |      |  |     ├─icon-image
|  |    |    |      |  |     |     ├─const.ts
|  |    |    |      |  |     |     ├─index.modules.less
|  |    |    |      |  |     |     ├─index.tsx
|  |    |    |      |  |     |     ├─images
|  |    |    |      |  |     |     |   └right.png
|  |    |    |      |  |     ├─icon-font
|  |    |    |      |  |     |     ├─const.ts
|  |    |    |      |  |     |     ├─demo.css
|  |    |    |      |  |     |     ├─demo_index.html
|  |    |    |      |  |     |     ├─iconfont.css
|  |    |    |      |  |     |     ├─iconfont.eot
|  |    |    |      |  |     |     ├─iconfont.js
|  |    |    |      |  |     |     ├─iconfont.json
|  |    |    |      |  |     |     ├─iconfont.svg
|  |    |    |      |  |     |     ├─iconfont.ttf
|  |    |    |      |  |     |     ├─iconfont.woff
|  |    |    |      |  |     |     ├─iconfont.woff2
|  |    |    |      |  |     |     ├─index.modules.less
|  |    |    |      |  |     |     ├─index.tsx
|  |    |    |      |  |     |     └name.ts
|  |    |    |      |  |     ├─head
|  |    |    |      |  |     |  ├─h2.tsx
|  |    |    |      |  |     |  ├─h3.tsx
|  |    |    |      |  |     |  ├─h4.tsx
|  |    |    |      |  |     |  └index.modules.less
|  |    |    |      |  |     ├─empty
|  |    |    |      |  |     |   ├─const.ts
|  |    |    |      |  |     |   ├─index.modules.less
|  |    |    |      |  |     |   ├─index.tsx
|  |    |    |      |  |     |   ├─images
|  |    |    |      |  |     |   |   ├─contacts.png
|  |    |    |      |  |     |   |   ├─data.png
|  |    |    |      |  |     |   |   ├─grade.png
|  |    |    |      |  |     |   |   ├─internet.png
|  |    |    |      |  |     |   |   ├─location.png
|  |    |    |      |  |     |   |   ├─message.png
|  |    |    |      |  |     |   |   ├─record.png
|  |    |    |      |  |     |   |   └update.png
|  |    |    |      |  |     ├─drop-down
|  |    |    |      |  |     |     ├─index.modules.less
|  |    |    |      |  |     |     ├─index.tsx
|  |    |    |      |  |     |     ├─types.tsx
|  |    |    |      |  |     |     ├─components
|  |    |    |      |  |     |     |     ├─select
|  |    |    |      |  |     |     |     |   ├─index.modules.less
|  |    |    |      |  |     |     |     |   └index.tsx
|  |    |    |      |  |     ├─divider
|  |    |    |      |  |     |    ├─const.ts
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    └index.tsx
|  |    |    |      |  |     ├─date-picker
|  |    |    |      |  |     |      ├─const.ts
|  |    |    |      |  |     |      ├─index.modules.less
|  |    |    |      |  |     |      └index.tsx
|  |    |    |      |  |     ├─citys-picker
|  |    |    |      |  |     |      ├─citys.ts
|  |    |    |      |  |     |      ├─const.ts
|  |    |    |      |  |     |      ├─index.module.less
|  |    |    |      |  |     |      ├─index.tsx
|  |    |    |      |  |     |      └untils.ts
|  |    |    |      |  |     ├─checkbox
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    ├─index.tsx
|  |    |    |      |  |     |    └list.ts
|  |    |    |      |  |     ├─carousel
|  |    |    |      |  |     |    ├─index.modules.less
|  |    |    |      |  |     |    ├─index.tsx
|  |    |    |      |  |     |    └item.tsx
|  |    |    |      |  |     ├─button
|  |    |    |      |  |     |   ├─const.ts
|  |    |    |      |  |     |   ├─index.modules.less
|  |    |    |      |  |     |   └index.tsx
|  |    |    |      |  |     ├─badge
|  |    |    |      |  |     |   ├─index.modules.less
|  |    |    |      |  |     |   └index.tsx
|  |    |    |      |  |     ├─avatar
|  |    |    |      |  |     |   ├─const.ts
|  |    |    |      |  |     |   ├─index.module.less
|  |    |    |      |  |     |   └index.tsx
|  |    |    |      |  |     ├─action-sheet
|  |    |    |      |  |     |      ├─const.ts
|  |    |    |      |  |     |      ├─index.modules.less
|  |    |    |      |  |     |      └index.tsx
|  |    |    ├─request
|  |    |    |    ├─package.json
|  |    |    |    ├─src
|  |    |    |    |  ├─const.ts
|  |    |    |    |  ├─utils.ts
|  |    |    |    |  ├─web
|  |    |    |    |  |  ├─fetch.ts
|  |    |    |    |  |  └index.ts
|  |    |    |    |  ├─taro
|  |    |    |    |  |  ├─fetch.ts
|  |    |    |    |  |  └index.ts
|  |    |    |    |  ├─react-native
|  |    |    |    |  |      ├─fetch.ts
|  |    |    |    |  |      └index.ts
|  |    |    ├─event-emitter
|  |    |    |       ├─index.ts
|  |    |    |       └package.json
|  |    |    ├─decorator
|  |    |    |     ├─package.json
|  |    |    |     ├─src
|  |    |    |     |  ├─components
|  |    |    |     |  |     └index.ts
|  |    |    ├─aliyun
|  |    |    |   ├─index.ts
|  |    |    |   ├─package.json
|  |    |    |   ├─src
|  |    |    |   |  ├─config.ts
|  |    |    |   |  ├─taro.ts
|  |    |    |   |  └web.ts
|  ├─custom-tab-bar
|  |       └index.tsx
|  ├─components【组件（全局组件，全局方法）】
|  |     ├─_template
|  |     |     ├─index.module.less
|  |     |     └index.tsx
|  |     ├─utils【公用函数】
|  |     |   └index.ts
|  |     ├─taro【Taro函数修改】
|  |     |  └index.ts
|  |     ├─tab-bar【自定义导航栏】
|  |     |    ├─index.modules.less
|  |     |    ├─index.tsx
|  |     |    ├─images
|  |     |    |   ├─sop-cgdd-hover.png
|  |     |    |   └sop-cgdd.png
|  |     ├─request【请求组件】
|  |     |    └index.ts
|  |     ├─loadMore
|  |     |    ├─index.module.less
|  |     |    ├─index.tsx
|  |     |    ├─images
|  |     |    |   ├─empty.png
|  |     |    |   └loading.gif
|  |     ├─assets【放置公用静态文件】
|  |     |   ├─images
|  |     |   |   ├─icon-customer-select.png
|  |     |   |   ├─icon-customer-selected.png
|  |     |   |   ├─icon-index-select.png
|  |     |   |   ├─icon-index-selected.png
|  |     |   |   ├─icon-main-select.png
|  |     |   |   └icon-main-selected.png
|  |     ├─aliyun
|  |     |   └index.ts
|  ├─common
|  |   └func.tsx
├─node_modules-cover【node_modules覆盖目录】
|         ├─.empty
|         ├─@tarojs
|         |    ├─webpack-runner
|         |    ├─router
|         |    |   ├─index.js
|         |    |   ├─LICENSE
|         |    |   ├─package.json
|         |    |   ├─types
|         |    |   |   └index.d.ts
|         |    |   ├─dist
|         |    |   |  ├─index.esm.js
|         |    |   |  └index.js
├─doc【文件】
|  └keng.md【开发中踩过的坑】
├─dist【编译结果目录】
|  ├─app.js
|  ├─app.json
|  ├─app.wxss
|  ├─common.js
|  ├─common.wxss
|  ├─project.config.json
|  ├─runtime.js
|  ├─sitemap.json
|  ├─vendors.js
|  ├─pages
|  |   ├─login
|  |   |   ├─index.js
|  |   |   ├─index.json
|  |   |   ├─index.wxml
|  |   |   ├─index.wxss
|  |   |   ├─images
|  |   |   |   └logo.png
|  |   ├─home
|  |   |  ├─index.js
|  |   |  ├─index.json
|  |   |  ├─index.wxml
|  |   |  ├─index.wxss
|  |   |  ├─scoll.js
|  |   |  ├─scoll.json
|  |   |  ├─scoll.wxml
|  |   |  └scoll.wxss
|  |   ├─cancelList
|  |   |     ├─index.js
|  |   |     ├─index.json
|  |   |     ├─index.wxml
|  |   |     └index.wxss
|  ├─components
|  |     ├─loadMore
|  |     |    ├─index.js
|  |     |    ├─index.json
|  |     |    ├─index.wxml
|  |     |    ├─index.wxss
|  |     |    ├─images
|  |     |    |   └empty.png
├─config【配置文件】
|   ├─dev.js
|   ├─index.js
|   └prod.js
├─.git
|  ├─config
|  ├─description
|  ├─HEAD
|  ├─index
|  ├─packed-refs
|  ├─refs
|  |  ├─tags
|  |  ├─remotes
|  |  |    ├─origin
|  |  |    |   └HEAD
|  |  ├─heads
|  |  |   └master
|  ├─objects
|  |    ├─pack
|  |    |  ├─pack-13b10344b4b516c012247396f744743697f57b93.idx
|  |    |  └pack-13b10344b4b516c012247396f744743697f57b93.pack
|  |    ├─info
|  ├─logs
|  |  ├─HEAD
|  |  ├─refs
|  |  |  ├─remotes
|  |  |  |    ├─origin
|  |  |  |    |   └HEAD
|  |  |  ├─heads
|  |  |  |   └master
|  ├─info
|  |  └exclude
|  ├─hooks
|  |   ├─applypatch-msg.sample
|  |   ├─commit-msg.sample
|  |   ├─fsmonitor-watchman.sample
|  |   ├─post-update.sample
|  |   ├─pre-applypatch.sample
|  |   ├─pre-commit.sample
|  |   ├─pre-merge-commit.sample
|  |   ├─pre-push.sample
|  |   ├─pre-rebase.sample
|  |   ├─pre-receive.sample
|  |   ├─prepare-commit-msg.sample
|  |   ├─push-to-checkout.sample
|  |   └update.sample