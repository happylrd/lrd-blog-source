---
title: Youbo项目总结
date: 2017-07-08 10:06:09
tags:
- Spring
- Vue
- Android
- React
categories:
- 技术向
thumbnail: http://cdn.happylrd.com/image/gaoyue_1.jpeg
---

> 横看成岭侧成峰，远近高低各不同。不识庐山真面目，只缘身在此山中。
> <div style="text-align:right"><p>——《<cite>题西林壁</cite>》</p></div>

## 引子

## 简介

### 架构

![Youbo项目架构图](http://cdn.happylrd.com/image/youbo_architecture.png)

```viz
graph youbo {
     desktop_web -- API
     mobile_web -- API
     android_app -- API
     cms -- API
     API -- api_server
     api_server -- image_server
     api_server -- database
     api_server -- cache
     cache -- database
}
```

### 项目类别

项目代号 | 类型 | 核心技术栈
------ | ---- | ---
[Iris](https://github.com/happylrd/youbo-api)   | API Server | Spring
[Seria](https://github.com/happylrd/youbo-desktop)  | Desktop&Mobile Web | Vue
[kiri](https://github.com/happylrd/youbo-cms)   | CMS | React
[Daphne](https://github.com/happylrd/youbo-android) | Android APP | Android

**注意**：*Iris* 与 *Seria* 目前未开源...

## 附录

- [Youbo项目文档](https://github.com/happylrd/youbo-docs)

（未完待续...）
