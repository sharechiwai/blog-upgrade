---
title: Setup ESLint
date: 2021-12-10
summary: This post note down the process of setup ESLint on a node js project
---
## ESLint

最近開始玩多好多 `NodeJS` project  
很多時候都有一些basic 既野要setup, e.g `ESLint / Prettier/ Unit Test` 等等  
今日想記錄低如何在`NodeJS` set up `ESLint`

首先我們要安裝 ESLint 相關package
```bash
npm install eslint eslint-config-prettier eslint-config-standard --save-dev

## 之後執行以下指令 去設定 ESLint 的 basic config
## 會自動產生一個 .eslintrc.json
npx eslint --init
```

以下是我的 ESLint config `.eslintrc.json`
```json
{
  "env": {
    "commonjs": true,
    "es2021": true,
    "node": true
  },
  "extends": ["eslint:recommended", "standard", "prettier"],
  "parserOptions": {
    "ecmaVersion": 12
  },
  "rules": {}
}
```

更新`package.json` 係 `Script` section
```json
 "scripts": {
    "lint": "eslint --ext .js ."
  },
```

最後我們可以在 command prompt 執行以下指令去 run eslint
```bash
npm run lint
```
Hope you find it useful
