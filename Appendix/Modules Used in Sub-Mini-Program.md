# Modules Used in Sub-Mini-Program



## Cancel List

文件路径：`helphub-sub-mini-program\src\pages\cancelList\index.tsx`

```tsx
import { View, Image } from '@tarojs/components'; *//容器&图片导入*
```

- `View`
  - Taro框架定义的微信小程序视图容器组件“视图容器”
  - 路径：`helphub-sub-mini-program\node_modules\@tarojs\components\types\Image.d.ts`
  - https://developers.weixin.qq.com/miniprogram/dev/component/view.html

- `Image`
  - Taro框架定义的微信小程序媒体组件“图片”
  - 路径：`helphub-sub-mini-program\node_modules\@tarojs\components\types\View.d.ts`
  - https://developers.weixin.qq.com/miniprogram/dev/component/image.html



```tsx
import Taro, { useState, usePullDownRefresh, useEffect, useReachBottom, useRouter } from '@tarojs/taro'; *//Hooks*
```

- `useState`
  - Taro框架定义的Hooks，功能应该与React自带的 `useState` Hooks类似
  - 路径:`helphub-sub-mini-program\node_modules\@tarojs\taro\src\hooks.js`
  - https://reactjs.org/docs/hooks-reference.html#usestate

- `usePullDownRefresh`
  - Taro框架定义的微信小程序页面UI下拉刷新Hooks
  - 路径：
    - `helphub-sub-mini-program\node_modules\@tarojs\taro\src\hooks.js`
    - `helphub-sub-mini-program\node_modules\@tarojs\taro\types\api\ui\pull-down-refresh.d.ts`
  - https://developers.weixin.qq.com/miniprogram/dev/api/ui/pull-down-refresh/wx.stopPullDownRefresh.html
  - https://developers.weixin.qq.com/miniprogram/dev/api/ui/pull-down-refresh/wx.startPullDownRefresh.html

- `useEffect`
  - Taro框架定义的Hooks，功能应该与React自带的 `useEffect` Hooks类似
  - 路径：`helphub-sub-mini-program\node_modules\@tarojs\taro\src\hooks.js`
  - https://reactjs.org/docs/hooks-reference.html#useeffect

- `useReachBottom`
  - Taro框架定义的微信小程序页面UI上拉触底Hooks
  - 路径：`helphub-sub-mini-program\node_modules\@tarojs\taro\src\hooks.js`

- `useRouter`

  - Taro框架定义的，用于微信小程序获取页面传入路由相关参数

  - 路径：`helphub-sub-mini-program\node_modules\@tarojs\taro\src\hooks.js`

    

```tsx
import * as styles from './index.module.less'; *//less文件的网页呈现设定*
```

- 本页面的less网页设置文件
- 路径：`helphub-sub-mini-program\src\pages\cancelList\index.module.less`



```tsx
import { get } from '~/components/request'; *//微盟自己写的组件：请求（应该是和服务器交互获取数据）*
```

- 与数据库联系，进行参数修改的组件
- 路径：`helphub-sub-mini-program\src\components\request\index.ts`



```tsx
import classNames from 'classnames'; 
```

- 路径：
  - `helphub-sub-mini-program\node_modules\classnames\index.d.ts`
  - `helphub-sub-mini-program\node_modules\@tarojs\components\types\common.d.ts`



```tsx
import LoadMore from "~/components/loadMore" *//微盟自己写的组件：自动加载列表中的对象*
```

- 微盟自己写的组件
- 路径：`helphub-sub-mini-program\src\components\loadMore\index.tsx`



```tsx
import { Toast, wx } from '~/common/func'; *//微盟自己写的组件：弹窗*
```

- `Toast`
  - 微盟自己写的弹窗组件
  - 路径：`helphub-sub-mini-program\src\common\func.tsx`
- `wx`
  - 微盟自己写的跳转组件
  - 路径：`helphub-sub-mini-program\src\common\func.tsx`





## Home

Notice: 这里只把和Cancle List页面中不同的依赖列了出来

文件路径：`helphub-sub-mini-program\src\pages\home\index.tsx`

```tsx
import { View, Image, Text } from '@tarojs/components'; //容器 & 图片 & 文字导入
```

- `Text`
  - Taro框架定义的微信小程序的基础内容组件“文本”
  - 路径：`helphub-sub-mini-program\node_modules\@tarojs\components\types\Text.d.ts`
  - https://developers.weixin.qq.com/miniprogram/dev/component/text.html



```tsx
import Taro, { useEffect, useState, usePullDownRefresh, useReachBottom, useDidShow } from '@tarojs/taro'; //Hooks
```

- `useDidShow`
  - Taro框架定义的微信小程序，页面展示时的回调Hooks
  - 路径：`helphub-sub-mini-program\node_modules\@tarojs\taro\src\hooks.js`



```tsx
import * as styles from './index.module.less'; //less文件的网页呈现设定
```

- 本页面的less网页设置文件
- 路径：`helphub-sub-mini-program\src\pages\home\index.module.less`



```tsx
import ScollFloor from "./scoll" //页面滚动功能的实现
```

- 该页面滚动功能的实现
- 路径：`helphub-sub-mini-program\src\pages\home\scoll.tsx`



```tsx
import LoadMore from "~/components/loadMore" //微盟自己写的组件：自动加载列表中的对象
```

- 微盟自己写的页面加载组件
- 路径：`helphub-sub-mini-program\src\components\loadMore\index.tsx`





## Login

Notice:这里只把和Cancle List 以及 Home 页面中不同的依赖列了出来

文件路径：`helphub-sub-mini-program\src\pages\login\index.tsx`

```tsx
import { View, Image, Input } from '@tarojs/components';
```

- `Input`
  - Taro框架定义的微信小程序的表单组件“输入框”
  - 路径：`helphub-sub-mini-program\node_modules\@tarojs\components\types\Input.d.ts`
  - https://developers.weixin.qq.com/miniprogram/dev/component/input.html



```tsx
import Taro, { login, useEffect, useState } from '@tarojs/taro';
```

- `login`
  - Taro框架定义的微信小程序的账号登录Hooks，用于获取用户登录状态的信息
  - 路径：`helphub-sub-mini-program\node_modules\@tarojs\taro\types\api\open-api\login.d.ts`



```tsx
import * as styles from './index.module.less';
```

- 本页面的less网页设置文件
- 路径：`helphub-sub-mini-program\src\pages\login\index.module.less`



```tsx
import { isNewIphone } from '~/modules/@wmeimob/taro-design/src/components/utils';
```

- 微盟自己写的新手机判定组件
- 路径：`helphub-sub-mini-program\src\modules\@wmeimob\taro-design\src\components\utils\index.ts`



```tsx
import { throttle, Toast, wx } from '~/common/func';
```

- `throttle`
  - 微盟自己写的节流函数
  - 路径：`helphub-sub-mini-program\src\common\func.tsx`

