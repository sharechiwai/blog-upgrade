---
type: "post"
title: "apt-get update - public key is not available"
date: 2021-03-08T00:00:00+08:00
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
  - Kali Linux
  - Ethical Hacking
---

嘗試在 `Raspbian` 上加入 Kali Linux Repository Source List  
但是在使用 `sudo apt-get update ` 時卻出現以下的 Error

```bash
The following signatures couldnt be verified because the public key is not available: NO_PUBKEY ED444FF07D8D0BF6
Reading package lists... Done
W: GPG error: http://kali.cs.nctu.edu.tw/kali kali-rolling InRelease: The following signatures couldnt be verified because the public key is not available: NO_PUBKEY ED444FF07D8D0BF6
E: The repository http://http.kali.org/kali kali-rolling InRelease is not signed.
N: Updating from such a repository cant be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
```

![signatures couldnt be verified because the public key is not available](/media/2021/public-key-not-avaliable-error.png "signatures couldnt be verified because the public key is not available)

**解決方法**
我們可以使用以下 command 去加入這個 key

```bash
gpg --keyserver pgpkeys.mit.edu --recv-key [KEY_SHOWN_WHICH_NOT_AVAILABLE_NO_PUBKEY]
gpg -a --export [KEY_SHOWN_WHICH_NOT_AVAILABLE_NO_PUBKEY] | sudo apt-key add -
```

![add public key command](/media/2021/fix-public-key-not-avaliable-command.png "add public key command")

e.g.

```bash
gpg --keyserver pgpkeys.mit.edu --recv-key  ED444FF07D8D0BF6
gpg -a --export ED444FF07D8D0BF6 | sudo apt-key add -
```

![fixed public key is not available issue](/media/2021/fix-public-key-not-avaliable-result.png "fixed public key is not available issue")
Hope you find it useful
