---
layout: post
title: 【Keefe.Studio】主播聚合搜索系统
category : project
tagline: "原创"
tags : Python 垂直搜索
keywords: [主播]
description: 主播聚合搜索的项目说明
date: 2016-9-30
---
### 系统说明
#### 软件需求源
  主播聚合搜索的需求灵感来自于本人观看直播时选择主播时的不爽感受，有时从直播平台推荐页进入的直播间并不是我想看的类型，而一些有特色的实力新主播不能及时发现。

  这种现象出现的原因有
  - 某些平台/主播存在刷礼物刷在线数粉丝的现象，表面上主播人气很高，实质是虚假的。
  - 签约主播会有公司进行包装，人气会比更有实力但未签约的独立主播更高。

#### 软件功能描述
- 数据范围：采集了国内人气最高的22家直播平台，目前约130万条主播数据。
- 检索：可通过主播昵称和直播间标题进行检索。
- 主播按原始数据项排序：对已采集到的主播按人气值、粉丝数、最近直播时间进行全网或者单个平台内排序。
- 主播按网红指数排序：综合考虑人气值、粉丝数、直播时长等计算网红指数。网红指数能更准确判断出一个主播的真正受欢迎程度。
- 主播按类别排序：类别可分游戏、娱乐、体育和科技等
- 排名榜：每天定时计算一次全网的主播总排名新主播排名，也可按类别进行单项排名。通过排名榜即可判断当前的热门主播，也可发现有潜力的新主播。


#### 数据处理流程
- 本搜索系统的Spider从各直播平台实时采集在线直播间数据，数据项有直播间类别、主播收到的礼物数、粉丝数等等。
- 系统后台对采集数据进行清洗（主要是数据类型转化），处理，入库。
- 每天闲时计算一次网红指数。

#### 项目相关需求
- 直播后台录制客户端：目前大多数平台不提供录制功能。
- 开发手机应用：在同一应用中观看不同平台的直播。
- 刷粉刷在线数的直播作弊检测系统


#### coding: Keefe Wu
### [项目地址](http://www.wuqifu.cn/www_show/getanchor/)
{% include JB/setup %}

- 原始排序 ![]({{BLOG_IMG}}anchor_getanchor.png)
- 网红排序 ![网红排序]({{BLOG_IMG}}anchor_getrank.png)
- 主播总榜 !主播总榜[]({{BLOG_IMG}}anchor_top_rank_0.png)
- 30天新主播总榜 ![30天新主播总榜]({{BLOG_IMG}}anchor_top_rank_type0_new30.png)
- 30天新娱乐主播总榜 ![30天新娱乐主播总榜]({{BLOG_IMG}}anchor_top_rank_type1_new30.png)