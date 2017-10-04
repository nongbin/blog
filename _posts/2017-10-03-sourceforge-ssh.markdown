---
layout: post
category: "linux"
title:  "sourceforge使用ssh登录"
tags: [sourceforge,ssh]
---
### 第一步，安装需要程序:

>下载putty压缩包，###安装过程略###

>官网： http://www.putty.org/（墙）  
>官网：https://www.chiark.greenend.org.uk/~sgtatham/putty/（无墙）       
 

### 第二步，配置putty

>1.下载putty压缩包， 
>
>2.找到压缩包里面的PUTTYGEN.EXE， 
> 
>3.打开PUTTYGEN.EXE，点击Generate生成密钥，
>  
>4.复制key（后面有用）保存密钥（save public key）一般保存到桌面，容易找到，
>  
>5.回到sourceforge.net，登录自己的账户，找到https://sourceforge.net/auth/shell_services这个是需要上一步复制的密钥，login shell选择：/bin/bash，ssh public key：复制粘贴进来，点击save 保存，  
>
>6.做好了前期的准备工作，回到putty的压缩包，找到PUTTY.EXE，打开之后host name填写：shell.sourceforge.net，port选择：22，connection type选择：ssh ，  
>
>7.接上面一步，找到左边的category，connection，ssh（不需要展开），第一次使用ssh登录sourceforge需要在ssh-remote command 输入“create”其他不变， 最后导入保存在桌面的密钥展开ssh，auth（不需要展开）最后一行，点击browser，导入保存在桌面的密钥，回到session，需要保存的自己命名。点击save ，最后点击open登录进去，输入你的用户名，密码（不显示）。  


### 第三步，目录的普及:

1,用户目录: /home/users/首字母/首2字母/用户名

2,project 在： /home/project-web/PROJECTNAME/, cgi-bin定向到网页/cgi-bin/下. htdocs就是网站根目录。

3,files 位置： /home/frs/project/PROJECTNAME/

4,用户的主页: /home/user-web/USERNAME/, 里面也有cgi-bin和htdocs

