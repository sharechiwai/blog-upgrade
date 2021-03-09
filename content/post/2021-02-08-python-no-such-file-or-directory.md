---
title: "'python' no such file or directory"
date: 2021-02-08T00:00:00+08:00
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
  - python
---

嘗試安裝 `wifite` 時出現了一個 python 的 error  
`'python' no such file or directory`
!['python' no such file or directory](/media/2021/usr-bin-env-python-no-such-file-or-directory.png "'python' no such file or directory")

解決方法十分簡單  
我們只需要安裝 `python-is-python3`

```bash
sudo apt-get install python-is-python3
```

![fixed - 'python' no such file or directory](/media/2021/usr-bin-env-python-no-such-file-or-directory-fix.png "fixed - 'python' no such file or directory")
Hope you find it useful
