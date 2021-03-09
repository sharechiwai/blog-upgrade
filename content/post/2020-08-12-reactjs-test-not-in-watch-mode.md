---
title: "Create-React-App test without watch mode"
date: 2020-08-12T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - Javascript
  - ReactJs
  - Code Playground
tags:
  - ReactJs
  - Unit Test
  - Open Source
---

最近嘗試在 `React App` 上加入 `Coverage Report`...  
可能是因為是用了`create-react-app`
所以在使用 `yarn test` 的時候便自己加了 watch mode..
![create-react-app test](/media/2020/create-react-app-test-watch-mode.png "create-react-app test")
當有 code change 時便會再 test 一次..  
在 console 上不停顯示 code coverage 便很繁忙了  
如果可以在 run code coverage report 時停了 watch 便好

**解決方法**
我們只需要加上 `--watchAll=false` 便不會執行 watch mode

e.g.

```
yarn test --watchAll=false
```

![create-react-app test without watch mode](/media/2020/create-react-app-test-without-watch-mode.png "create-react-app test without watch mode")

Hope you find it useful
