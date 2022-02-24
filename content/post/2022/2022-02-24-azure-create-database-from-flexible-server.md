---
title: How to create database from azure flexible server
date: 2022-02-24
summary: azure flexible server create database via cli
tags:
  - Azure
  - Azure Flexible Server
  - Postgres Database
---
今日想同大家分享 如何在azure flexible server 建立Database  
同一個 Azzure Flexible Server 上是可以建立多過 database 的

**解決方法:**

```bash
### 首先要login azure 
az login

### 之後assign subscription Id
### 因為有機會同一個 Azure login 入面
### 會有多過一個subscription
az account set --subscription  [subscription id]

### Create database command
### server name 是你在建立 azure flexible server 時填的那一個
### 沒有`postgres.database.azure.com` 的
az postgres flexible-server db create -d [Database name] --resource-group [resource group name] --server-name [server name]
```

hope you find it useful
