---
title: "RaspberryPi unzip file via 7Zip"
date: 2021-02-13T00:00:00+08:00
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
  - 7Zip
  - Unzip
---

在 Linux / Ubuntu 上如何 unzip a Zip file

**解決方法**  
我們可以安裝 `7Zip` 之後用 command extract 便可

**安裝 7Zip**

```bash
sudo apt-get install p7zip-full
```

![install 7zip on linux](/media/2021/install-7zip.png "install 7zip on linux")

**Unzip file**

```bash
sudo 7z e wordlist.zip
```

![use 7zip to unzip / extract zip file on linux](/media/2021/unzip-via-7zip.png "use 7zip to unzip / extract zip file on linux")
Hope you find it useful
