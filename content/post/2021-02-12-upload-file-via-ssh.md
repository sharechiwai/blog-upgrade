---
title: "upload copy file via ssh"
date: 2021-02-12T00:00:00+08:00
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
  - upload file
  - ssh
---

如何從 local machine 經 `ssh` 去 copy 檔案到 `raspberrypi` 上  
**解決方法**十分簡單...

我可以使用 scp command  
`scp [File to Copy] [Destination]`

```bash
scp "C:/Users/Chi/Desktop/kali/wordlist.zip" pi@raspberrypi.local:/home/pi/Documents/wordlists
```

![copy file from local machine via ssh to remote](/media/2021/scp-copy.png "copy file from local machine via ssh to remote")

Hope you find it useful
