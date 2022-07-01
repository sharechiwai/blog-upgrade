---
title: You are running `create-react-app` 5.0.0, which is behind the latest release (5.0.1)
date: 2022-04-13T04:37:20.556Z
summary: Solved You are running `create-react-app` 5.0.0, which is behind the latest release (5.0.1)
tags:
  - ReactJs
  - create-react-app
---
今日想起個新既reactjs project 時出現了這個error message
```
$ npx create-react-app .

You are running `create-react-app` 5.0.0, which is behind the latest release (5.0.1).

We no longer support global installation of Create React App.

Please remove any global installs with one of the following commands:
- npm uninstall -g create-react-app
- yarn global remove create-react-app

The latest instructions for creating a new app can be found here:
https://create-react-app.dev/docs/getting-started/

```

**解決方法:**
```bash
npx react-native init [project name]

```

hope you find it useful
