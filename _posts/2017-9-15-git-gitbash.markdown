---
layout: post
category: "git"
title:  "windows7使用git bash"
tags: [window,git,github,gitbash]
---

#  windows7使用git bash  

> 本文教程结合GitHub的官方帮助文档 https://help.github.com/articles/set-up-git/


### 第一步，下载git，安装，过程略（不会的自己百度）官网：https://git-scm.com/downloads  Tip：下载需要fq，不然速度感人


### 第二步，使用gitbahs工具生产ssh keys，  
```
打开gitbash，输入“ssh-keygen -t rsa -b 4096 -C "your_email@example.com"” 修改成自己的邮箱，中间一直按回车就行，自己看反馈信息，会有ssh keys的存放路径，找到“id_rsa.pub”，全选，复制，打开GitHub，登陆自己的账号，找到setting-----ssh and gpg keys ----自己添加一个ssh keys ---粘贴自己刚刚复制的keys   https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/
```

### 第三步，设置用户名   
>  1. 打开git bash   
>  2. 输入命令 “$ git config --global user.name "Mona Lisa"” Tip：Mona Lisa 修改为自己的名字
>　3. 验证用户名“$ git config --global user.name ”   官方文档： https://help.github.com/articles/setting-your-username-in-git/


### 第三步，设置邮箱   
>  1. 打开git bash   
>  2. 输入命令 “$ git config --global user.email "email@example.com""” 
>  Tip：email@example.com 修改为自己的邮箱 
>    
>　3. 验证用户名“$ git config --global user.email ”     官方文档： https://help.github.com/articles/setting-your-commit-email-address-in-git/  






