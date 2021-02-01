---
title: "How to run reactjs in different port"
date: 2021-01-30:00:00+08:00
author: ShareChiWai
layout: post
categories:
  -
tags:
  - ReactJs
  - create-react-app
---

最近用了`NodeJs Express` 來做 Web App 的 Backend 用左 port `3000`  
而`create-react-app` 既 default port 又係 `3000`  
怎樣可以改變`create-react-app` 既 port 呢

**解決方法**:
十分簡單... 我們只需要在 `package.json` 上既 scripts section  
`start` 上加上 `set PORT=[PORT_YOU_WANTED]` 便可  
e.g.

```json
 "scripts": {
    "start": "set PORT=9000 && react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "lint": "eslint . --ext .js --ext .jsx --ignore-path .gitignore --cache"
  },

```

Hope you find it useful
https://stackoverflow.com/questions/750172/how-to-change-the-author-and-committer-name-and-e-mail-of-multiple-commits-in-gi
