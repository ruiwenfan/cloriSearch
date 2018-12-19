[English Version](README.md)

cloriSearch<div id="top"></div>
==========

作为一套面向广告业务设计的检索引擎内核，cloriSearch致力于解决常规业务开发中的策略检索与在线广告匹配问题，为中小互联网公司商业变现提供一套开源的广告检索技术方案。

* [主要特性](#features)
* [设计思想](#design)
* [使用实例](#usage)
* [安装说明](#install)
* [待完成列表](#todo)
* [作者](#authors)

## 主要特性<div id="features"></div>

cloriSearch目前支持简单倒排检索、范围检索、LBS检索等三种检索场景(基本能cover除搜索广告之外的其他广告定向条件)，这三类检索场景的具体内涵是指

* 简单倒排检索 - 最基础的检索方式，term的值是一个有限集合，比如 city ∈ {北京, 上海, 深圳}，gender ∈ {male}或者device ∈ {iOS}
* 范围检索 - 广告定向条件是一个数值区间，比如"时间从2018-12-01 00:00 ~ 2018-12-20 00:00"，"年龄在18 ~ 25之间的用户"，"流量序号在20 ~ 50之间"
* LBS检索 - 基于地理位置(经纬度)的广告定向，比如检索出以某经纬度为圆心、某距离为半径圈定的圆形范围内的定投广告

## 设计之路<div id="design"></div>

cloriSearch在设计与工程实现上参考了多个开源项目与相关技术论文，包括

* *[Indexing Boolean Expressions](http://theory.stanford.edu/~sergei/papers/vldb09-indexing.pdf)* - 斯坦福大学发表的布尔表达式检索论文，是cloriSearch所采用的核心广告检索算法
* [Lucene](http://lucene.apache.org/) - 倒排链求交集技术
* [Redis](https://github.com/antirez/redis.git) - LBS定向参考并引入了redis对geohash实现
* [brpc](https://github.com/brpc/brpc.git) - json与protobuf的互相转换
* [cloriSkip](https://github.com/shpilu/cloriSkip.git) - 跳跃表实现

此外，还部分参考了大型互联网公司的广告检索技术实现(未开源，多靠推断)，包括

## 使用实例<div id="usage"></div>


## 安装说明<div id="install"></div>


## 待完成列表

## 作者 <div id="authors"></div>

* James Wei (weijianlhp@163.com)   

[返回顶部](#top)

