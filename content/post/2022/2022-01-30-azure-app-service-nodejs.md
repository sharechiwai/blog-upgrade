---
title: Deploy NodeJs express site to Azure App Service
date: 2022-01-30
summary: This post share how to deploy nodejs express site to Azure App Service
---
最近開始使用 `Microsoft Azure App Service`  
去host 一個 NodeJS express 既 web service  
誰不知當我deploy 時常常都出現問題  

**解決方法**  
十分簡單  
只要在 `Configuration` section 入面  
`General settings` 既 `Startup Command` 入面  
輸入怎樣 start 你的 nodejs express server 既command  

我的example 是
`node index.js`

不用加其他設定 e.g. `Application setting`  
除了你的application 入面有用到 `environment variable`  
那你便需要把這些 setting 加進 `Application setting` 入面  

Hope you find it useful