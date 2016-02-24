---
layout: post
title: Linux下的expect的下载和安装
category: 技术
date: 2011-12-15 16:24:12
tags: expect linux
---


Expect是在Tcl基础上创建起来的，它还提供了一些Tcl所没有的命令，它可以用来做一些linux下无法做到交互的一些命令操作，在远程管 理方面发挥很大的作用。

`spawn`命令激活一个Unix程序来进行交互式的运行。
`send`命令向进程发送字符串。
`expect` 命令等待进程的某些字符串。
`expect`支持正规表达式并能同时等待多个字符串，并对每一个字符串执行不同的操作.

## Tcl 安装
主页: <http://www.tcl.tk>  
下载地址: <http://www.tcl.tk/software/tcltk/downloadnow84.html>

 1. 下载源码包  
 
 	wget http://nchc.dl.sourceforge.net/sourceforge/tcl/tcl8.4.11-src.tar.gz
	
 2. 解压缩源码包
 
	tar xfvz tcl8.4.11-src.tar.gz
	
 3. 安装配置
 
	cd tcl8.4.11/unix
	./configure –prefix=/usr/tcl –enable-shared
	make
	make install
	
安装完毕以后，进入tcl源代码的根目录，把子目录unix下面的tclUnixPort.h copy到子目录generic中。
暂时不要删除tcl源代码，因为expect的安装过程还需要用。

## expect 安装 (需Tcl的库)
主页: <http://expect.nist.gov/>

 1. 下载源码包
 
	wget http://sourceforge.net/projects/expect/files/Expect/5.45/expect5.45.tar.gz/download
	
 2. 解压缩源码包

	tar xzvf expect5.45.tar.gz
	
 3. 安装配置
 
	cd expect5.45
	./configure –prefix=/usr/expect –with-tcl=/usr/tcl/lib –with-tclinclude=../tcl8.4.11/generic
	make
	make install
	ln -s /usr/tcl/bin/expect /usr/expect/bin/expect
 
## 参考链接
  * <http://blog.chinaunix.net/space.php?uid=20639775&do=blog&id=2453085>

