---
title: "Linux常用基础命令"
date: 2021-08-12T20:44:59+08:00
slug: linux-command
image: linux.png
draft: false
tags: [blog,linux,ubuntu]
categories: blog
weight: -500
---

# Linux常用基础命令

## 前提

```shell
#带[]为可选参数，使用命令是应该取代[]
```

## 路径操作

**显示当前所在路径**

```shell
pwd
```

**更换路径**

```shell
cd path  
#当前目录可用.表示
#上一级使用..表示
#cd -可进入上次所在路径
```

**显示当前目录所有文件或文件夹**

```shell
ls [-a][-h][-l]
#或者
ls [-ahl] #常用
#-a 查看当前目录下的所有目录和文件（包括隐藏的文件）
#-l 列表查看当前目录下的所有目录和文件（列表查看，显示更多信息）
#-h 配合-l使用可以以人性化方式显示文件大小
```

------

## 文件与文件夹

**创建一个文件**

```shell
touch 文件名 
#示例 touch test.txt在当前目录创建一个名为test.txt的文件
```

**创建一个文件夹**

```shell
mkdir 文件夹名
```

**复制文件夹**

```shell
cp 要复制的文件 目标路径
#实例 cp test.txt .   复制test.txt到当前目录   
```

**移动文件**

```shell
mv 要移动的文件 目标路径
#示例mv test.txt ~ 移动test.txt到home目录下
```

**查看文件**

```shell
cat 文件名
#示例 cat test.txt
```

**删除文件**

```shell

rm 文件    # 删除当前目录下的文件
rm -rf* 文件或或文件夹    #rm [-rf] 目录
rm -rf *  # 将当前目录下的所有目录和文件全部删除
rm -rf /*   # 【自杀命令！慎用！慎用！慎用！】将根目录下的所有文件全部删除
```

------

## 基本命令

### 1.1 关机和重启

关机

```shell
   shutdown -h now     立刻关机
   shutdown -h 5     5分钟后关机
   poweroff       立刻关机
```

重启

```shell
  shutdown -r now     立刻重启
   shutdown -r 5     5分钟后重启
   reboot         立刻重启
```

### 1.2 帮助命令

```shell
--help命令
 shutdown --help：
 ifconfig  --help：查看网卡信息
```

 

```shell
man命令（命令说明书） 
 man 指令
 注意：man 打开命令说明书之后，使用按键q退出
```

------



## su、sudo

### su

su用于用户之间的切换。但是切换前的用户依然保持登录状态。如果是root 向普通或虚拟用户切换不需要密码，反之普通用户切换到其它任何用户都需要密码验证。

```shell
1. su test:切换到test用户，但是路径还是/root目录
2. su - test : 切换到test用户，路径变成了/home/test
3. su : 切换到root用户，但是路径还是原来的路径
4. su - : 切换到root用户，并且路径是/root
```

**su不足**：如果某个用户需要使用root权限、则必须要把root密码告诉此用户。

退出返回之前的用户：exit

### sudo

sudo是为所有想使用root权限的普通用户设计的。可以让普通用户具有临时使用root权限的权利。只需输入自己账户的密码即可。

------



## 清屏

命令：

```shell
clean
```

## 打包和压缩

**Windows的压缩文件的扩展名  .zip/.rar**
**linux中的打包文件：aa.tar    
linux中的压缩文件：bb.gz   
linux中打包并压缩的文件：.tar.gz**

命令：

```shell
tar -zcvf #打包压缩后的文件名 要打包的文件
#其中：
 z：调用gzip压缩命令进行压缩
 c：打包文件
 v：显示运行过程
 f：指定文件名
```

## 解压

```shell
tar [-zxvf] 压缩文件   
#其中：x：代表解压
```

------



## apt命令

```shell
sudo apt-get update  #更新源
sudo apt-get install package #安装包
sudo apt-get remove package #删除包
sudo apt-cache search package #搜索软件包
sudo apt-cache show package  #获取包的相关信息，如说明、大小、版本等
sudo apt-get install package --reinstall  #重新安装包
sudo apt-get -f install  #修复安装
sudo apt-get remove package --purge #删除包，包括配置文件等
sudo apt-get build-dep package #安装相关的编译环境
sudo apt-get upgrade #更新已安装的包
sudo apt-get dist-upgrade #升级系统
sudo apt-cache depends package #了解使用该包依赖那些包
sudo apt-cache rdepends package #查看该包被哪些包依赖
sudo apt-get source package  #下载该包的源代码
sudo apt-get clean && sudo apt-get autoclean #清理无用的包
sudo apt-get check #检查是否有损坏的依赖
```



------

## gedit文本编辑器

```shell
gedit 文件名
#示例 gedit test.txt
```

## 进入root

```shell
sudo -i
然后提示输入密码回车
```

