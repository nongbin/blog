---
layout: post
category: "git"
title:  "使用SourceTree推送代码到Github出现UTF-8错误失败"
tags: [git,github,sourcetree,error]
---


# 使用SourceTree推送代码到Github出现UTF-8错误失败

> Failure:The file"推送文件目录及文件" is not properly UTF-8 encoded（推送文件目录及文件，这个是你本地项目推送的路径）

# 解决的办法

> 使用notepad++ 打开文件，然后修改格式（格式-转化为UTF-8无BOM编码格式），再重新推送一次即可