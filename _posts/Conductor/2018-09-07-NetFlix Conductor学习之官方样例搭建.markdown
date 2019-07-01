---
layout: post
title: NetFlix Conductor学习之官方样例搭建!
date:  2018-09-07
Author: XKZ
categories: jekyll update
tags: [Conductor]
comments: true
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这个系列的文章主要是老大让本人学校微服务编排，将之运用到我们现有的一个项目中，由于本人初接触，对其中的一些内容没有深入了解，所以在学习之初，先将官网的样例进行运行。下面就介绍下NetFlix Conductor官方样例搭建过程。
<h2>一、下载源码</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;首先我们到NetFlix Conductor的git官网将源码下载下来，下载地址：https://github.com/Netflix/conductor
<h2>二、安装Swagger API</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;首先进入到我们的安装路径下，运行ce server 进入server目录，接着运行../gradlew server命令开始安装过程，整个安装过程比较耗时。
![img](https://xukaizhong188.github.io/xukaizhong.github.io/assets/postImages/2018-09-07/pic1.jpg)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;注意一下：安装UI要求先node.js 8.0以上因为运行glup命令是需要node.js。安装完node.js需要安装gulp
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;安装步骤：
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;执行cd ui 进入ui目录，
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;再执行 gulp watch等待构建完成即可。


