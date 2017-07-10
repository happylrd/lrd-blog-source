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
     Desktop_Web -- API
     Mobile_Web -- API
     Android_APP -- API
     CMS -- Internal_API
     API -- API_Server
     Internal_API -- API_Server
     API_Server -- Image_Server
     API_Server -- Cache
     API_Server -- Database
     Cache -- Database
}
```

### 项目类别

项目代号 | 类型 | 核心技术栈
--- | --- | ---
[Iris](https://github.com/happylrd/youbo-api)       | API Server  | Spring
[Seria](https://github.com/happylrd/youbo-desktop)  | Desktop Web | Vue
[Metis](https://github.com/happylrd/youbo-mobile)   | Mobile Web  | Vue
[Daphne](https://github.com/happylrd/youbo-android) | Android APP | Android
[kiri](https://github.com/happylrd/youbo-cms)       | CMS         | React

**注意**：*Iris*、*Seria* 和 *Metis* 目前未开源...

## 附录

- [Youbo项目文档](https://github.com/happylrd/youbo-docs)

（未完待续...）
