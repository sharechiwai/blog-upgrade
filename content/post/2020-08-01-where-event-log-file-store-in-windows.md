---
title: "Where Event Log files store on Windows - Event Log 檔案在那裡"
date: 2020-08-01T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  - Windows
  - 電腦小貼事 Computing Tips and Tricks
tags:
  - Event Log
---

最近用了`Windows Defender` 的 `offline mode` 來 scan 電腦睇下有無中毒...  
有時電腦有 Error 都可以使用 `Windows` 的 `Event Viewer`  
睇返個 `Event Log` 去了解下出現什麼問題...

有時候開啟 `Event Viewer` 時由於太多 log 既關係...  
所以要 load 很久... 還有..有時想睇既 Log 可能好難搵...  
![Event Viewer](/media/2020/event-viewer.png "Event Viewer")

如果可以直接開啟負責既 `Event log` file 這便應該會更簡單直接...  
那麼 `Event Log` file 存在那裡呢?  
大家可以輸入以下的路俓去開啟 `Event Log` 的資料夾..  
之後便可以自行打開相關的 Log 了  
`%windir%\System32\winevt\Logs`

![Event Log folder](/media/2020/event-log-files-folder.png "Event Log folder")

Hope you find it useful
