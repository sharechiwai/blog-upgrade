---
title: "SQL Server Management Studio (SSMS) shortcut to view Table Defination (sp_help)"
date: 2020-11-03T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  -
tags:
  - Microsoft SQL Server
  - SSMS
  - TSQL
---

最近同事介紹左個好正既 SQL Server Management Studio (SSMS) 既 Shortcut key  
用來 檢視 Table defination / information of database object  
我們只需要在 Query 上 highlight Table 名 之後按 `ALT+F1`  
便可以看到相關係資訊  
e.g. 我用了 `master.dbo.MSreplication_options` 來做例子  
功能和 `sp_help tablename` 一樣

![SSMS ALT + F1](/media/2020/ssms_alt_f1.png "SSMS ALT + F1")

Hope you find it useful
