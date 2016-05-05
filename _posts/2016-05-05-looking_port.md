---
layout: post
title: "查看本地端口"
date: "2016-05-05 23:40:37 +0800"
tags: [端口, 命令, linux]
---

在开发中经常需要查看本地相应的端口是否运行相应的服务，netstat和netcat可以用来做这样的工作

## 使用netstat

<pre>
$ netstat -antlp |grep 4000
tcp        0      0 127.0.0.1:4000          0.0.0.0:*               LISTEN      10058/ruby2.3   
tcp        1      0 127.0.0.1:60496         127.0.0.1:4000          CLOSE_WAIT  11924/chrome    
tcp        0      0 127.0.0.1:4000          127.0.0.1:60496         FIN_WAIT2   -               
tcp        0      0 127.0.0.1:60498         127.0.0.1:4000          TIME_WAIT   -               
</pre>
最后一行是对应的端口号，在上面的例子中，jekyll的服务端运行在10058端口

也可以使用netmap和netcat命令来扫描端口。netcat功能很丰富, 相当于网络版的cat。
