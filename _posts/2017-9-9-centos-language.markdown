---
layout: post
category: "linux"
title:  "����centos��ʾ����"
tags: [linux,language]
---

#  �鿴��ǰϵͳ����
<����½linuxϵͳ�򿪲����ն�֮������ echo $LANG���Բ鿴��ǰʹ�õ�ϵͳ����
#  �鿴��װ�����԰�
<���鿴�Ƿ����������԰��������ն����� locale�������zh cn ��ʾ�Ѿ���װ����������

#  �������û���������Կɽ���yum install��װ
< yum groupinstall chinese-support������������ͨ�������������أ��ϴ���ȥ�ɣ�

```
#  �޸�ϵͳ����Ϊ����
					Vi  /etc/sysconfig/i18n ��ע��ĺ�֮������һ��ϵͳ��
					����һ���޸�ΪLANG="zh_CN.UTF-8"
```