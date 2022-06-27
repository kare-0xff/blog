---
title: "如何快速获取ssh Key密钥"
date: 2021-08-12T15:21:45+08:00
slug: get-sshkey
image: sshkey.png
draft: false
tags: [ssh]
categories: blog
weight: -500
---

# 如何快速获取ssh Key密钥

## 正文

1. 在git bash执行一下指令

2. 

   ```sh
   git config --global user.email "you@example.com"
   git config --global user.name "Your Name"
   ```

3. 生成shh key

   ```sh
   ssh-keygen -t rsa
   ```

4. 一路回车就行

5. 默认会生成在目录

   ```sh
   C:\Users\用户名\.ssh
   ```

6. 获取生成目录下id_rsa.pub里的密钥就能使用了
