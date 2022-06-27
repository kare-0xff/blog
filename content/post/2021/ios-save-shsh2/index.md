---
title: "IOS备份shsh2指南"
date: 2021-08-17T11:00:39+08:00
slug: ios-save-shsh2
image: shsh.png
draft: false
tags: [shsh2]
categories: ios
weight: -500
---

# IOS备份shsh2指南

## 什么是shsh2

SHSH Blob 是非官方为便于今后 iDevice 设备降级而准备的备用数字签名字符串；

如何通过 Tsssaver 及 Telegram 来查找 Blob 并下载备份保存

SHSH 是基于缩写: signed hash 和 binary large object。为签名序列和二进制对象。也称为 ECID SHSH。每个 Blob 都与一个特定的设备绑定在一起，数据使用设备的 ECID 进行编码。

SHSH Blob 是一个非官方术语，指的是苹果生成并用于个性化每个 iOS 设备的 IPSW 固件文件的数字签名。它们是 Apple 协议的一部分，旨在确保在设备上安装受信任的软件，通常仅允许安装最新的 iOS 版本。苹果对此过程的公开名称是系统软件授权。

SHSH 是 iOS 10 之前的名称，之后称为 SHSH2。

## shsh的作用

iOS升级与降级的必需品，但是也会受到sep的限制

## 备份shsh

### 爱思助手备份

1. 手机连接电脑 
2. 电脑打开爱思助手-刷机越狱-专业刷机 
3. 点击【查询适配版本】即可备份 
4. 点击【下载SHSH】即可查询是否备份成功

------

### **TSS Saver备份**

> 对于未越狱的设备，您将需要使用“计算机”方法。

#### **使用 TSS Saver App 保存 Blob**

1. 在您首选的[包管理器](https://ios.cfw.guide/package-managers)[中将 repo.1conan.com](https://repo.1conan.com/)添加到您的源中
2. 下载并安装 TSS Saver
3. 如果您在 iOS 14 上使用 unc0ver，请下载并安装 libkrw
4. 如果您在 iOS 14 上使用 Taurine。请下载并安装 libkernrw
5. 点击“保存 Blob”
6. 收到确认信息后，点击“打开”

> 出现新的 blob 可能需要一些时间，尤其是在服务器负载不足的情况下。一般都需要科学上网。

------



#### 使用 TSS Saver 网站保存 Blob

> A12+ 用户将需要他们的 ApNonce 和 Generator 对来使用此方法。

获取 Generator 和 ApNonce（仅限越狱 A12+）

1. 如果您在 iOS 14 上使用 unc0ver，请安装 libkrw

2. 如果您在 iOS 14 上使用 Taurine，请安装 libkernrw

3. 打开终端应用程序并运行 

   ```plaintext
   sudo dimentio > dimentio.txt
   ```

   - 或者，您可以从 TSS Saver App 的 Generator 选项卡中获取您的 Generator 和 ApNonce

4. 转到 Filza 中的 /var/mobile 并打开 dimentio.txt

5. 复制`Current nonce is`文本文件底部后面的 0x 数字以及`entangled nonce:`. 0x 数是你的 Generator，纠缠的 nonce 数是你的 ApNonce。把这些东西放在安全的地方，以后你会用到

开始保存 Blob

1. 将您的 iOS 设备连接到 Mac 或 PC
2. 打开 iTunes 或 Finder
   - Windows 用户必须下载[普通版本而](https://www.apple.com/itunes/)不是 Windows 应用商店版本
3. 导航到设备摘要页面
4. 单击序列号字段两次
   - 这应该会更改以显示您的 ECID 号码
5. 记下此 ECID 号码，以便稍后阅读
6. 打开[TSS Saver 网站](https://tsssaver.1conan.com/v2/)
7. 输入您的设备 ECID
8. 选择您的设备
   - iPhone 6S、6S Plus 和 iPhone SE 用户需要通过[下载此应用程序](https://itunes.apple.com/us/app/ax-cpu/id1048174418?mt=8)来获取他们的主板配置
   - A12+ 用户需要输入 ApNonce 和 Generator 对
9. 点击提交

------

#### 使用 blobsaver 保存 Blob

**blobsaver**

1. 下载、安装和启动最新版本的[blobsaver](https://github.com/airsquared/blobsaver/releases)
2. 将您的 iOS 设备连接到您的计算机并确保它已解锁
3. 单击第一个“从设备读取”按钮，该按钮将填写您的 ECID 和设备信息
4. 如果您的 iOS 设备不是 A12 或更高版本，则不需要获取 APNonce，您可以跳过下一步

**获取特定于设备的 APNonce 和生成器**

确保您的设备在整个过程中已连接并解锁。

1. 单击 APNonce 字段旁边的第二个“从设备读取”按钮
2. 如果您已越狱或已在您的设备上设置了生成器/apnonce 对，您想保留，请选择“越狱”。否则，选择“越狱”

您的设备将多次重启进入恢复模式。当您重新启动到正常操作系统模式时，解锁您的 iOS 设备。

如果您陷入恢复模式，请尝试使用 blobsaver 中“帮助”菜单中的“退出恢复模式”选项。

无论您是否越狱，都可以随时重复使用这些值来保存 blob。

**保存 Blob**

1. 填写完所有信息后，单击“Go”以保存 blob
2. 也可以单击“保存设备”来保存您当前设备的信息，以便以后再次为其保存 blob

