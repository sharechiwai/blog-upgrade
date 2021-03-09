---
title: "RaspberryPi how to unzip unrar"
date: 2021-02-11T00:00:00+08:00
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
  - unrar
  - Linux Troubleshooting
---

如何在 raspbian 上 unzip a rar 檔案 / 安裝 `unrar`

**解決方法:**

首先我們要更改 `sources.list`

```bash
sudo nano /etc/apt/sources.list
```

![sudo nano /etc/apt/sources.list](/media/2021/nano-source-list.png "sudo nano /etc/apt/sources.list")

uncomment 以下那一行

```
deb-src http://raspbian.raspberrypi.org/raspbian/ buster main contrib non-free rpi
```

![uncomment deb-src non-free](/media/2021/uncomment-deb-src-non-free.png"uncomment deb-src non-free")
執後執行 `apt-get update` 和 `apt-get install unrar-free`

```bash
sudo apt-get update
sudo apt-get install unrar-free
```

![apt-get install unrar-free](/media/2021/install-unrar-free.png"apt-get install unrar-free")

之後便可以 執行 `unrar e [filename]` 去 un-rar 檔案了

```bash
unrar e wordlist.rar
```

![extract a rar file](/media/2021/extract-rar-file.png"extract - unrar a rar file")

Hope you find it useful
