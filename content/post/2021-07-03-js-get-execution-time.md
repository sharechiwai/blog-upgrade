---
title: "How to get/check javascript execution time"
date: 2021-07-03T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - Javascript
tags:
  - js
  - performance
---

最近開始睇下D algorithm 既 tutorial  
想了解下學左 / 用左會 efficient 幾多呢  
這個當然要用時間來 value  

最簡單既方法就係計 execution time  
在`javascript` 上如何計execution time 呢?  


** 解決方法 **

我們可以使用
```javascript
console.time();
console.timeEnd();
```
來記錄 javascript 的 execution time
e.g.
```javascript
// created a delay function to simulate a slow process
const delay = ms => new Promise(res => setTimeout(res, ms));

// create a time to log full execution time
console.time('full');

// create a time to log the 3s process
console.time('log 3s');
await delay(3000);
console.log('3s');
console.timeEnd('log 3s');

console.time('log 5s');
await delay(5000);
console.log('5s');
console.timeEnd('log 5s');

console.time('log 10s');
await delay(10000);
console.log('10s');
console.timeEnd('log 10s');

// print the full execution time
console.timeEnd('full');
```

gist
https://gist.github.com/sharechiwai/00256c8fd2c01c6849fb25f70782def5

Hope you find it useful
