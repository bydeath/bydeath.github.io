---
layout: post
title: "vim-jekyll插件"
date: "2016-04-29 02:16:55 +0800"
tags: vim jekyll vim插件
---

这是一个对 vim-jekyll插件的测试，可以用vim命令来方便的写博客。

## 新建一个博文
```
!Jpost! vim-jekyll
```
在vim的命令命令模式下执行`!Jpost! vim-jekyll`就可以在_post目录下面新建一个格式为`2016-05-06-vim-jekyll.md`的文件, 并且在文件的开头自动写入下面的头部。

<pre>
---
layout: post
title: "a"
date: "2016-05-05 23:24:06 +0800"
---
</pre>

## 启动jekyll服务端
```
Jserve
```
`Jserve`命令在后台启动服务端，之后就可以在浏览器端输入127.0.0.0:4000来随时预览博文。这条命令相当于执行了 `jekyll serve -s BLOG_ROOT -d BLOG_ROOT/SITE_DIR <args>` 。

## 其他命令
* 头部的模板可以通过变量`g:jekyll_post_template`来修改。
* `Jserve`命令在后台的命令可以通过`g:jekyll_serve_command`变量来自定义。
