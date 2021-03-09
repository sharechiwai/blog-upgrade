---
title: "add-apt-repository: command not found"
date: 2021-02-05T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - Linux
  - Ubuntu
tags:
  - Linux
  - Ubuntu
  - RaspberryPi
  - RaspberryPi4
  - rp4
  - Monitor
  - Linux Troubleshooting
---

嘗試加入新的 package repository 時出現了以下 error  
`add-apt-repository: command not found`  
![fixed - add-apt-repository: command not found](/media/2021/add-apt-repository.png "fixed - add-apt-repository: command not found")

**解決方法:**
加了`software-properties-common` 便可

```bash
sudo apt-get install software-properties-common
```

Hope you find it useful
