---
title: "git rewrite commit author"
date: 2021-02-01T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  -
tags:
  - git
---

最近發現自己有些 Git Repository 的 Git Author name 用錯了 account  
![git commit history with author name](/media/2021/git-batch-amend-commit-author-name.png "git commit history with author name")
忘記了在 clone repo 既時候要用

```bash
git config user.name "sharechiwai"
git config user.email "MY_EMAIL"
```

要找些方法去改變舊 commit 上的 Author name  
做了一會 research 之後終於找到了

**解決方法:**
我們可以執行以下 `git` command 去 update 整個 repository 上的 Author name, Author email, committer name 和 committer email

```bash
git filter-branch -f --env-filter "GIT_AUTHOR_NAME='YOUR_GIT_NAME'; GIT_AUTHOR_EMAIL='YOUR_GIT_EMAIL'; GIT_COMMITTER_NAME='YOUR_GIT_NAME'; GIT_COMMITTER_EMAIL='YOUR_GIT_EMAIL';" HEAD

```

![git commit rewrite author name](/media/2021/git-batch-amend-commit-author-name-process.png "git commit rewrite author name")
e.g.

```bash
git filter-branch -f --env-filter "GIT_AUTHOR_NAME='sharechiwai'; GIT_AUTHOR_EMAIL='YOUR_GIT_EMAIL'; GIT_COMMITTER_NAME='sharechiwai'; GIT_COMMITTER_EMAIL='YOUR_GIT_EMAIL';" HEAD

```

![git commit rewrite author name success](/media/2021/git-batch-amend-commit-author-name-success.png "git commit rewrite author name")

Hope you find it useful
