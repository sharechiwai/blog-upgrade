---
title: "ASP.Net MVC client-side validation"
date: 2020-07-30T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - ASP Net MVC
tags:
  - DotNet
  - ASP Net MVC
---

好耐都無掂過 ASP.Net MVC...  
之前有朋友叫我幫佢睇下個 project  
發現佢個 Registration Form 有個小小問題..  
就係唔識行 `Client-side Validation`  
每次按 `Register` button 都會 做一個 Post  
之後先會出現.. Validation Error message

睇左佢個 Model , Controller 同 View (.cshtml)  
都沒有問題...
再花多了一些時間.. 終於發現那裡出現問題了...

**解決方法**
我們只需要在 `View/Shared/_Layout.cshtml` 加入 `JQuery`的 `Validation` library 便可  
e.g.

```javascript
    <script src="~/lib/jquery/dist/jquery.min.js"></script>
    <script src="~/lib/jquery-validation/dist/jquery.validate.min.js"></script>
    <script src="~/lib/jquery-validation-unobtrusive/jquery.validate.unobtrusive.min.js"></script>
```

Hope you find it useful
