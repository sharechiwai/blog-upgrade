---
title: "ReferenceError: regeneratorRuntime is not defined jest nodejs"
date: 2020-07-25T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - NodeJs
tags:
  - NodeJs
  - Jest
  - Unit Test
---

今日係 NodeJs 上用 Jest 寫 Unit Test 時出現了以下錯誤信息  
`ReferenceError: regeneratorRuntime is not defined`

![ReferenceError: regeneratorRuntime is not defined](/media/2020/regeneratorRuntime-is-not-defined.png "ReferenceError: regeneratorRuntime is not defined")

**解決方法:**  
只要在 NodeJs Project 上安裝 `babel-polyfill` package  
之後在 Unit Test file 上 import babel-polyfill 便可
e.g.

```
import 'babel-polyfill';
import JokeHelper from './JokeHelper';

test('Call Test Joke function', () => {
  expect(JokeHelper.test()).toBe('test joke');
});

```

另一個更好的解決方法..我們可以在 `jest config` 上設定一些常用的 library  
這樣我們便不用每一個 files 都 import 了

以下是我的`jest.config.js` setting

```
module.exports = {
  verbose: true,
  setupFiles: ['<rootDir>/jest.init.js'],
};

```

`jest.init.js`

```
import 'babel-polyfill';
```

Hope you find it useful
