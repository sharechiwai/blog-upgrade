---
title: "How to resume SSH session - Ubuntu / RaspberryPi"
date: 2021-02-06T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - Linux
  - Ubuntu
tags:
  - Linux
  - ssh
  - Ubuntu
  - RaspberryPi
  - RaspberryPi4
  - rp4
  - Raspbian
---

最近最左塊 `RaspberryPi4` 諗住用黎比屋企人做 Media Center  
但係就咁放係度做 media center 好似有 D 浪費  
所以便安裝左 D tools 黎玩  
發現有 D tools run 既時候需要 一些時間  
但係當你個 `ssh` connection 斷左之後...
你在 terminal 上執行既 command 亦都會被 cancel  
怎樣才可以 reconnect / resume ssh session 呢?

解決方法十分簡單  
我們只需要安裝 `screen`

```bash
sudo apt-get install screen
```

之後用以下 `command` 去 ssh 到 raspberrypi / linux 便可

```bash
ssh -t <server.domain.name> screen -R
```

e.g.

```bash
ssh -t pi@raspberrypi.local screen -R
```

Hope you find it useful
