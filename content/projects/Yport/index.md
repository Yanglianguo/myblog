---
title: "Yport使用常见问题"
description: "Linux系统下的权限问题"
---

## Linux 下提示“无法执行文件”

在部分 Linux 系统中，通过拷贝或下载方式获得的可执行文件默认不具备执行权限。
请在终端中执行：

	chmod +x Yport

然后再运行程序。  
	
或者通过右键属性,勾选可执行权限。

---

## Linux 下无法打开串口（权限不足）

Linux 系统中，串口设备通常归属于dialout 等用户组，普通用户默认没有访问权限。
可通过以下方式解决：
	
	sudo usermod -aG dialout $USER
	
执行后需重新登录或重启系统才能生效。
