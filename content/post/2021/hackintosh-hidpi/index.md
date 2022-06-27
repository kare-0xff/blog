---
title: "黑苹果开启原生Hidpi"
date: 2021-08-20T17:50:55+08:00
slug: hackintosh-hidpi
image: hidpi.png
draft: false
tags: [hidpi]
categories: blog
weight: -500
---

# 黑苹果开启原生Hidpi

## 黑苹果命令下开启原生HiDPI

一条命令可开启接近原生的 HIDPI 设置，不需要 RDM 软件即可在系统显示器设置中设置，不过 RDM 有时候也是比较好用的，有些显示器不用开启，就可以在 RDM 里面选择一些带有 HiDPI 效果的分辨率。

**脚本的 Github 项目地址**: [GitHub - xzhih/one-key-hidpi: Enable macOS HiDPI](https://github.com/xzhih/one-key-hidpi)

终端下执行:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"
```

开启后重启生效！

> 如果你的设备不是黑苹果的话，那么请关闭 SIP 后再操作。

**如果执行失败呢？**

那么将项目克隆到本地并运行commond后缀的文件就可以了。