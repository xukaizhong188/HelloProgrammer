---
layout: post
title: NetFlix Conductor源码架构!
date:  2019-07-01
Author: XKZ
categories: jekyll update
tags: [Conductor]
comments: true
---
![img](https://xukaizhong188.github.io/HelloProgrammer/images/2019-07-01/pic1.png)
<h2>一、client</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;和conductor通信的客户端。
<h2>二、common</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;主要涉及task任务和workflow工作流的元数据和请求参数定义同时还包括一些工具类。
<h2>三、core</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;核心类，包括事件、队列功能类。还包括任务类型定义。每种类型任务的具体实现逻辑和映射关系。
<h2>四、jersey</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;主要提供swagger接口展示层，通过启动这个模块来看到接口列表。
<h2>五、es-persistence</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这一层主要是持久层，根据请求版本不同包括es5和es2二个模块，作用主要包括将任务和工作流元数据保存到es中，还有就是将任务运行时数据进行保存，比如任务执行的状态，执行时间等等。
<h2>六、mysql-persistence</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;mysql持久层，存储任务和工作流定义的元数据。
<h2>七、redis-persistence</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;redis持久层，存储任务和工作流定义的元数据。
<h2>八、server</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;负责conductor server端的启动、工作流任务的启动，由server层调用core层实现分布式状态机控制和任务的调度。
<h2>九、UI</h2>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;可视化任务管理界面，通过该界面能够看到任务和工作流定义的元数据和图形展现，以及工作流执行的状态情况。

 

