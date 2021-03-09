---
title: "How to untrack committed file - 如果在git 上 untrack committed file"
date: 2020-07-28T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - Git
tags:
  - Git
  - .gitignore
---

今日需要在 git 上去 `gitignore` 一個之前已經 commit 了既 file

**解決放法**  
我們可以使用以下 git command 去 untrack 之前 commit 左既 file

```
git rm --cached [filename]
```

e.g.

```
git rm --cached appsetting.Development.json
```

之後在 `.gitignore` 上加入你想 ignore 的檔案名便可

Hope you find it useful
