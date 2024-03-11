---
title: SVN的配置和使用
categories:
  - [学习, 工具]
date: 2024-03-06 16:52:04
tags:
---

# 引言
:::primary no-icon
目前开发这段时间以来 
大部分项目中使用的还是`Git`
但是仍存在使用`SVN`的情况 
`SVN`对与我来说比较陌生 
所以打算整理一下使用方法
:::

# SVN简介
SVN全称为[Apache Subversion]{.blue}，是一个开放源代码的版本控制系统。 
随着代码开发的进程，开发人员会把自己的代码数据上传到中央资料档案库`repository` 
这个档案库会根据版本记住每一次的代码 并支持回退

# SVN安装
> SVN分为服务端和客户端
而对于开发者而言 
只需要在电脑上安装SVN的客户端 
就可以从仓库中拉取代码

1. Windows
windows需要安装SVN软件 TortoiseSVN
> https://tortoisesvn.net/downloads.html

2. Linux
Linux只需要通过应用命令安装即可
```bash
# 这里展示一下Ubuntu的安装
sudo apt install subversion
```

# SVN操作
:::info no-icon
SVN安装完成之后进行一些基本操作
:::

1. Checkout 提取代码
> 将仓库里的代码提取到本地路径
```bash
# server_path指SVN的路径地址 
# local_path指本地路径
svn checkout server_path local_path

# 同时这个代码也支持简写
svn co s_p l_p
```


2. Commit 提交代码
3. Update 更新代码

