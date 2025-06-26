---
author: blake
pubDatetime: 2022-07-21T00:00:00Z
title: "linux下移动文件或目录用哪个命令"
postSlug: mv-cp
featured: false
draft: false
ogImage: ""
tags:
  - mv
  - cp
description: "linux下移动文件或目录用哪个命令"
---

# linux下移动文件或目录用哪个命令

linux下移动文件或目录用哪个命令？
这个看似简单的问题，里面存在很多细节

**mv命令的问题：**
mv 大文件夹时，假如命令中断，会导致部分文件没有被移动到目标文件夹。

> 笔者遇到过多次mv命令中断问题：移动过程中磁盘满了、部分文件没有读权限等等
>
> 如何解决mv中断后目标文件夹数据不完整，mv是不支持的。
> mv重要的几个参数：
> mv -b 参数支持 加过存在相同文件名则覆盖前会备份文件
> mv -f 强制覆盖目标文件内容

如果目标目录中存在源目录同样的子目录，mv是不支持移动的，会提示：`File exists`错误。

说到底mv只是个简单的rename操作而已。

对于移动文件夹、因为mv命令简单，所以用的还是比较多。但笔者已经在这个问题上吃过几次亏了

> docker lib目录一般在/var/lib目录中，因为机器root目录分配空间较小，当image和container多的时候root目录空间就满了，笔者已经出现过2次 用mv移动/var/lib 文件夹到大磁盘的操作，两次都是因为/var/lib有些子文件夹没有权限导致mv失败，失败后想用mv命令合并两边文件夹内容，发现只是徒劳

**如何安全的移动大文件夹:**
**`cp -r`**
linux安全移动大文件操作一定要用`cp -r` (`r`是递归)
`cp`命令也支持中断后文件内容合并
先cp再rm 是非常安全的操作

参考:
https://askubuntu.com/questions/269775/mv-directory-not-empty
