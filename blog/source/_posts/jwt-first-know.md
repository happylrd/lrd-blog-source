---
title: 当JWT遇上Spring Security
date: 2017-07-07 21:37:42
tags:
- JWT
- Spring
- Security
categories:
- 技术向
thumbnail: http://cdn.happylrd.com/image/jwt.jpg
---

> 黑云翻墨未遮山，白雨跳珠乱入船。卷地风来忽吹散，望湖楼下水如天。
> <div style="text-align:right"><p>——《<cite>望湖楼醉书</cite>》</p></div>

## 引子

## JWT简介

### 是什么

JWT（JSON Web Token）是一种开放标准（[rfc-7519](https://tools.ietf.org/html/rfc7519)），它定义了一种 *小巧且自包含* 的方式 用于将各方之间的信息作为 *JSON对象* 进行安全传输。由于数据进行了 *数字签名*，所以可以被验证和信任。JWT 可以使用 [HMAC](https://en.wikipedia.org/wiki/Hash-based_message_authentication_code) 算法对 secret 进行加密 或 使用 [RSA](https://zh.wikipedia.org/wiki/RSA%E5%8A%A0%E5%AF%86%E6%BC%94%E7%AE%97%E6%B3%95) 的 公钥/私钥对（public/private key pair） 来进行签名。

- 小巧：可以通过 URL、POST参数 或放在 HTTP header内部 发送，传输速度快。
- 自包含：payload（有效载荷）包含了有关用户的所有必需信息，从而避免多次查询数据库。

### 为什么


> 小学期（7月1日-7月14日）完后补充

（未完待续...）
