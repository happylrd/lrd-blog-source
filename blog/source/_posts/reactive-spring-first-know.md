---
title: 当反应式编程遇上Spring
date: 2017-07-16 09:10:26
tags:
- 反应式编程
- Spring
- 后端
categories:
- 技术向
thumbnail: http://cdn.happylrd.com/image/project_reactor.png
---

> 水光潋滟晴方好，山色空蒙雨亦奇。欲把西湖比西子，淡妆浓抹总相宜。
> <div style="text-align:right"><p>——《<cite>饮湖上初晴后雨</cite>》</p></div>

## 引子

> todo

## 简介

### 什么是反应式编程？

反应式编程（Reactive Programming）是与 数据流和变化传播 有关的 异步编程范式，它针对 **异步** 和 **事件驱动** 的 **非阻塞** 应用程序。

它需要少量线程用于纵向扩展（即在JVM内）而不是通过集群来进行横向扩展。

- 横向扩展：用更多的节点来支撑更大量的请求。
- 纵向扩展：提升一个节点的能力来支撑更大量的请求。

### Spring WebFlux模块

#### 服务器端

在服务器端，WebFlux 支持2种不同的编程模型：
- 基于注解
- 函数式，Java 8 lambda风格的 路由和处理

![WebFlux概览](http://cdn.happylrd.com/image/webflux_overview.png)

（未完待续...）
