---
title: Setup Prettier
date: 2021-12-11
summary: This post note down the process of setup Prettier on a node js project
---
## Prettier
```bash
npm install --save-dev prettier

```
建主一個 `.prettierrc.js` 檔案來做 `prettier` 的設定

之後便可以加入適合自己的config

```json
module.exports = {
  trailingComma: 'all',
  tabWidth: 2,
  semi: true,
  singleQuote: true,
};


```

在 `package.json` 加入以下設定

```bash
"scripts": {
    "format": "prettier check .",
    "fix-format": "prettier --write ."
  },
```
`format` 用來檢查有沒有什麼檔案需要再format

`fix-format` 是用`prettier` 去format 所有檔案

hope you find it useful