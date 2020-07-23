---
title: "FFmpeg - 十分好用可以轉換Audio / video既 program"
date: 2020-03-08T00:00:00+08:00
author: ShareChiWai
layout: post
categories:
  -
tags:
  - ffmpeg
  - Convert Video
  - Convert Audio
  - Free software
---

ffmpeg -i MAH08730.mp4 -filter:v "setpts=0.5*PTS" MAH08730_timelapse.mp4 -hwaccel cuda