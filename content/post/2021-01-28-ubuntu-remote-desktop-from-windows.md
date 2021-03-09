---
title: "Ubuntu remote desktop from windows 10"
date: 2021-01-28T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  -
tags:
  - Windows
  - Remote Desktop
  - Ubuntu
  - Linux
---

最近買了隻 `RaspberryPi 4` 想安裝 `Ubuntu` 來做一個 mini-computer  
給家人用來做`media centre`  
由於屋企沒有 電腦 Mon 所以 要試東西要連上 TV...  
有點麻煩 如果可以安裝 `Remote Desktop` 便好了

解決方法:

```bash
sudo apt install xrdp
sudo systemctl enable --now xrdp
sudo apt-get install mate-core
sudo ufw allow from any to any port 3389 proto tcp
```

Hope you find it useful
