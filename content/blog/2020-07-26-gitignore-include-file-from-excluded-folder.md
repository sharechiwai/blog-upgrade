---
title: ".gitignore include a file from excluded folder"
date: 2020-07-26T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - Git
tags:
  - Git
---

最近朋友介紹使用[Codecov](https://codecov.io/) 來顯示 project 上的 Unit Test 既 Code Coverage  
由於他需要把資料夾`coverage` 上的 一個檔案 `clover.xml` 放進 repository 上..  
但是 default 的 `.gitignore` 已經把 `coverage` 整個資料夾 exclude 了..  
那麼我們如何把在`.gitignore`已經 exclude 左既 folder 上的一個檔案 include 返去 git 入面呢?

**解決放法**
我們可以在`.gitignore` 上的 把 exclude folder 那一行 加`!` 變成不會 exclude ...  
e.g.

```
# original
coverage
```

變成 以下的 code

```
# 把 coverage folder 不 ignore
!coverage
# 再用以下的code 把coverage folder ignore
coverage/*
# 最後 specify 那一個在coverage folder內的file 不ignore 加上 便可
!coverage/clover.xml
```

Hope you find it useful
