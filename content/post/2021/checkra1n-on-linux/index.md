---
title: "CheckRa1n On Linux"
date: 2021-08-26T12:53:59+08:00
slug: checkra1n-on-linux
image: c1linux.png
draft: false
tags: [checkra1n]
categories: jailbreak
weight: -500
---

# CheckRa1n On Linux

## 前言

> Windows版的checkra1n还是不要想了，有没有macos
>
> 只能去舔一下Linux咯
>
> Linux的官方源里并没有checkra1n
>
> 以下命令均在shell中运行，以Ubuntu为例

### 第一条

```shell
#添加checkra1n软件源
echo 'deb https://assets.checkra.in/debian /' | sudo tee /etc/apt/sources.list.d/checkra1n.list
```

### 第二条

```shell
# 获取钥匙
sudo apt-key adv --fetch-keys https://assets.checkra.in/debian/archive.key
```

### 第三条

```shell
# 刷新软件源
sudo apt-get update
or
sudo apt update
```

### 第四条

```shell
安装checkra1n
sudo apt-get install checkra1n
or
sudo apt install checkra1n
```

### 补充

> 执行完以上四条命令后就安装了，checkra1n软件可以通过启动器直接打开
>
> 当然了，官网也贴心的准备了终端版本，
>
> 只需要在终端里输入checkra1n并回车会就出现终端版的checkra1n
>
> 但是该版本需要root权限，反正给root权限就完事了
>
> ```shell
> #进入root
> sudo -i 
> ```
>
> 输入密码回车就行，输入的时候看不见，直接输入就完事了，输完回车





