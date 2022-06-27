---
title: "使用OdysseyRa1n安装Sileo"
date: 2020-11-21T17:25:53+08:00
slug: install-sileo-by-odysseyra1n
image: odysseyra1n.jpg
draft: false
tags: [odysseyra1n]
categories: ios
weight: -500
---
# 使用OdysseyRa1n安装Sileo

## 简介

Odysseyra1n 是来自 Coolstar 的一个新的处理计划，并附带了来自 Diatrus 新的、开源的 Procursus bootstrap。

Odysseyra1n 能够让你的设施运转齐全自力的 libhooker。Libhooker 是 Coolstar 从零开端打造的一个以速率和稳固性为条件的 substrate/substitute。Libhooker 对 iOS 13 进行了完美的适配。

Procursus 从零开端就被计划为开源，一切人都能够拜访，并附带 Diatrus 不断在开辟的 133 个软件包，此中包含 wget2，这是一切 iOS Boostrap 的第一个软件包。Procursus 的计划目标是能够轻松地增加就任何越狱中，以便疾速、轻松地增加成为越狱依赖，而且依赖是古代化的、最新的。

Odysseyra1n 仅允从应用 checkra1n 越狱的设施，不允从 unc0ver 越狱设施。

## macOS 平台

在 macOS 的终端输入以下命令安装 homebrew，使用国内镜像源安装，如果电脑没有安装 Xcode 需要输入两次命令。第一次输入会提示安装系统更新，系统更新安装完成后，再次输入命令进行安装 homebrew，请耐心等待安装完成。

```sh
/bin/zsh -c "$(curl -fsSL https://gitee.com/cunkai/HomebrewCN/raw/master/Homebrew.sh)"
```

安装 homebrew 完成之后，再次输入命令安装 iproxy，请耐心等待安装完成。

```shell
brew install usbmuxd
```

## Linux 平台

终端输入命令安装 iproxy

```shell
sudo apt install libusbmuxd-tools
```

--------------------

### checkra1n 越狱

首先使用 checkra1n 越狱，如何越狱就不再赘述了。

> 如果已经使用 checkra1n 越狱，请先 rootfs 清理越狱环境再使用 checkra1n 越狱一次。

### 安装 Sileo

注意事项：使用 CoolStar 提供的脚本及国内分流脚本，不需要打开 SSH 通道，checkra1n 越狱后，**不要打开 checkra1n 安装 Cydia**。

### CoolStar 原版脚本

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/coolstar/Odyssey-bootstrap/master/procursus-deploy-linux-macos.sh)"
```

----

## 安装完后

### 更新插件（必须）

Sileo 刷新完成后，会提示更新插件，直接更新即可。

### 安装 libhooker（必须）

Sileo 切换至开发者模式（慢慢找，一个圆圆的按钮，不要找不到就说没有）

进入Odyssey Repo 安装 PreferenceLoader和libhook

**libhooker 安装完成后，请使用 checkra1n 重新引导越狱一次，或者安装 NewTerm (iOS 10 - 13) 终端插件，使用命令。**

```shell
su /etc/rc.d/libhooker
```

