---
title: "Hugo一键部署到Gitee或Github"
date: 2021-08-13T20:23:02+08:00
slug: onekey-deployment
image: hugo.png
draft: false
tags: [hugo]
categories: blog
weight: -500
---

# Hugo一键部署到Gitee或Github

为hugo博客创建一个一键推送到GitHub或gitee的.sh文件，前提是在对应的仓库已有ssh密钥

创建一个名为`deploy.sh`的文件并写入以下内容

```sh
hugo #构造你的blog

cd public #进入构造后的blog输出目录

git init #初始化git

git add -A

git commit -m 'deploy'

git push -f https://gitee.com/l1nsn0w/l1nsn0w.git master #向存储库推送

cd ../  # 回到上一级目录

rm -rf public # 删除目录
```

