---
layout: post
title: "python3 install configparser"
date: "2016-05-06 17:05:33 +0800"
tags: python3 configparser
---

Python3下面程序提示`ImportError: No module named 'ConfigParser'`, 我尝试用`pip3 install configparser`进行安装，但是提示语法错误。
<pre>
    SyntaxError: invalid syntax
    
    ----------------------------------------
Command "python setup.py egg_info" failed with error code 1 in /tmp/pip-build-be66_oen/configparser/
</pre>

后来使用[stackoverflow](https://stackoverflow.com/questions/14087598/python-3-importerror-no-module-named-configparser)中提到的方法来安装了python3-dev后，就以及装了configparser。直接导入就可以使用了。python3中ConfigParser改名为configparser了。

```
sudo apt-get install python3-dev
```
