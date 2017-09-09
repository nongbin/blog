---
layout: post
category: "linux"
title:  "Ŀ¼����h5ai��װ�̳�"
tags: [h5ai,centos]
---

# ��װlnmp
```
<��1.1��ʹ��putty�����Ƶ�SSH���ߵ�½VPS���������
��½�����У�screen -S lnmp
�����ʾscreen: command not found ������ڿ���ִ�У�yum install screen �� apt-get install screen��װ
#  1.2�����ز���װLNMPһ����װ��
<����װLNMP�ȶ���
<  wget -c http://soft.vpser.net/lnmp/lnmp1.4.tar.gz && tar zxf lnmp1.4.tar.gz && cd lnmp1.4 && ./install.sh lnmp
<  Ĭ�ϰ�װlnmp�ɲ�д������Ҫ��װLNMPA��LAMP����./install.sh ����Ĳ����滻Ϊlnmpa��lamp���ɡ����������վ�����ݿ�Ŀ¼���޸İ�װ��Ŀ¼�µ� lnmp.conf �ļ���
```
# h5ai����
< ��ַ�� https://larsjung.de/h5ai/

```
	2.1 ��������h5ai��������
	2.2���ú����������󣬱༭�������������ļ���
		vim /usr/local/nginx/conf/vhost/your_domain.conf
	2.3 �� root��һ�У���nginxΪ���ӣ�����Ϊ��
		index index.html index.php /_h5ai/public/index.php;
	2.4ȥ�������õ� PHP ������
		vim /usr/local/php/etc/php.ini
		������disable_functions�� ɾ���⼸��������scandir��exec��passthru������ӱ����õĺ�����ɾ����
		Tip��vim��������/ disable_functions�� set nu ��ʾ�к�
	2.5����lnmp
		lnmp restart 
	
```

# h5aiĿ¼
< ������ _h5ai
< ��   ������ CHANGELOG.md
< ��   ������ private
< ��   ������ README.md
< ������ ��Ҫ��ʾ���ļ���
< ��   ������ ���ļ���1
< ��   ������ �ļ�1
< ��   ������ �ļ�2
< ������ ��Ҫ��ʾ���ļ���
< ������ �ļ�1
< ������ �ļ�2


# ���� h5ai ���๦��
< ��ĿǰΪֹ��h5ai ��������ʹ���ˣ��������ǿ��Կ��� _h5ai ȫ�����ܡ�ͨ�� http(s)://your_domain/_h5ai/public/index.php ���Բ鿴 _h5ai ��ȫ�����ܿ��������Ĭ�������ǿյġ�

# options.json �еĸ��๦��
```
λ�� _h5ai/private/conf Ŀ¼�¡�

������أ�
���� ��download��
127 �У�enabled �� false ��Ϊ true��

�ļ���Ϣ����ά�룺
���� ��info��
185 �У�enabled �� false ��Ϊ true��

Ĭ�ϼ������ģ�
���� ��l10n��
202 �У�enabled �� false ��Ϊ true��

�ļ����ļ��ж�ѡ��
���� ��select��
323 �У�enabled �� false ��Ϊ true��
```

# ����ͼ����
```
 ͼƬ��
		�� _h5ai �У�private �� public �ļ����е� cache Ŀ¼����Ȩ��Ϊ 755��
 EXIF��
	  ͨ�� phpize ��װ PHP �� exif ģ�鼴�ɡ�
 ��Ƶ����ͼ��
			��װ FFmpeg ���ɡ�
 PDF ����ͼ��
			��װ ImageMagick��
```
# Shell tar��Shell zip��Shell du
< ȥ���� php.ini �б����ú��� exec�� passthru ���ɡ�����ȥ�����õ� scandir ����������У�����Ȼ�ᵼ���޷���ʾĿ¼��