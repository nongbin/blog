---
layout: post
category: "linux"
title:  "设置centos显示中文"
tags: [linux,language]
---

#  查看当前系统语言
<　登陆linux系统打开操作终端之后，输入 echo $LANG可以查看当前使用的系统语言
#  查看安装的语言包
<　查看是否有中文语言包可以在终端输入 locale命令，如有zh cn 表示已经安装了中文语言

#  如果本地没有中文语言可进行yum install安装
< yum groupinstall chinese-support（不能联网的通过其他电脑下载，上传上去吧）

```
#  修改系统语言为中文
					Vi  /etc/sysconfig/i18n （注意改好之后重启一下系统）
					将第一行修改为LANG="zh_CN.UTF-8"
```