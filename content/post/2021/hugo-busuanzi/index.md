---
title: "为hugo引入不蒜子"
date: 2021-08-18T21:19:29+08:00
slug: hugo-busuanzi
image: busuanzi.png
draft: false
tags: [hugo]
categories: blog
weight: -500
---

# 为hugo引入不蒜子

## 安装脚本（必选）

------

要使用不蒜子必须在页面中引入js

我的hugo引入js的路径：

> themes\stack\layouts\partials\head\head.html
>
> 其他都是大同小异

```js
<script async src="//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js">
</script>
```

## 显示站点总访问量

要显示站点总访问量，复制以下代码添加到你需要显示的位置。

> 举个栗子：比如我blog的首页底部那个统计就是将代码加在以下这个路径
>
> themes\stack\layouts\partials\footer\footer.html
>
> 其实都是大同小异的

有两种算法可选：

算法a：pv的方式，单个用户连续点击n篇文章，记录n次访问量。

```html
<span id="busuanzi_container_site_pv">
    本站总访问量<span id="busuanzi_value_site_pv"></span>次
</span>
```



算法b：uv的方式，单个用户连续点击n篇文章，只记录1次访客数。

```html
<span id="busuanzi_container_site_uv">
  本站访客数<span id="busuanzi_value_site_uv"></span>人次
</span>
```

## 写在最后

在本站的的footer已经引入了不蒜子计数器

