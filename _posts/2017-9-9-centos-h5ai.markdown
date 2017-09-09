---
layout: post
category: "linux"
title:  "目录程序h5ai安装教程"
tags: [h5ai,centos]
---

# 安装lnmp
```
<　1.1、使用putty或类似的SSH工具登陆VPS或服务器；
登陆后运行：screen -S lnmp
如果提示screen: command not found 命令不存在可以执行：yum install screen 或 apt-get install screen安装
#  1.2、下载并安装LNMP一键安装包
<　安装LNMP稳定版
<  wget -c http://soft.vpser.net/lnmp/lnmp1.4.tar.gz && tar zxf lnmp1.4.tar.gz && cd lnmp1.4 && ./install.sh lnmp
<  默认安装lnmp可不写，如需要安装LNMPA或LAMP，将./install.sh 后面的参数替换为lnmpa或lamp即可。如需更改网站和数据库目录先修改安装包目录下的 lnmp.conf 文件。
```
# h5ai官网
< 网址： https://larsjung.de/h5ai/

```
	2.1 官网下载h5ai，过程略
	2.2设置好虚拟主机后，编辑虚拟主机配置文件：
		vim /usr/local/nginx/conf/vhost/your_domain.conf
	2.3 将 root上一行（以nginx为例子），改为：
		index index.html index.php /_h5ai/public/index.php;
	2.4去除被禁用的 PHP 函数：
		vim /usr/local/php/etc/php.ini
		搜索”disable_functions“ 删除这几个函数”scandir、exec、passthru，将其从被禁用的函数中删除“
		Tip：vim搜索”：/ disable_functions“ set nu 显示行号
	2.5重启lnmp
		lnmp restart 
	
```

# h5ai目录
< ├── _h5ai
< │   ├── CHANGELOG.md
< │   ├── private
< │   └── README.md
< ├── 您要显示的文件夹
< │   ├── 子文件夹1
< │   ├── 文件1
< │   └── 文件2
< └── 您要显示的文件夹
< ├── 文件1
< └── 文件2


# 开启 h5ai 更多功能
< 到目前为止，h5ai 可以正常使用了，但是我们可以开启 _h5ai 全部功能。通过 http(s)://your_domain/_h5ai/public/index.php 可以查看 _h5ai 的全部功能开启情况，默认密码是空的。

# options.json 中的更多功能
```
位于 _h5ai/private/conf 目录下。

打包下载：
搜索 “download”
127 行，enabled 由 false 改为 true。

文件信息及二维码：
搜索 “info”
185 行，enabled 由 false 改为 true。

默认简体中文：
搜索 “l10n”
202 行，enabled 由 false 改为 true。

文件及文件夹多选：
搜索 “select”
323 行，enabled 由 false 改为 true。
```

# 略缩图功能
```
 图片：
		将 _h5ai 中，private 与 public 文件夹中的 cache 目录设置权限为 755。
 EXIF：
	  通过 phpize 安装 PHP 的 exif 模块即可。
 视频略缩图：
			安装 FFmpeg 即可。
 PDF 略缩图：
			安装 ImageMagick。
```
# Shell tar、Shell zip和Shell du
< 去除在 php.ini 中被禁用函数 exec与 passthru 即可。另外去除禁用的 scandir 函数（如果有），不然会导致无法显示目录。