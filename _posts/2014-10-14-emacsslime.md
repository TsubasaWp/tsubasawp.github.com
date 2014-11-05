---
layout: post
title: "emacs+slime开发环境配置"
description: ""
category: 
tags: []
---
{% include JB/setup %}

> **前言**: 这算是我第一篇正式的在emacs中用markedown写的blog...真是一步一坑啊...

###背景
最近比较闲, 打算搞搞lisp. 一开始用终端+clisp来写码, 但很快发现写超过3行就跪了..而且它没有自动缩进和配色. 所以打算折腾一下emacs+slime开发环境.

###Emacs
关于emacs本身这里不多说了...建议使用2.4以上版本, 否则加载slime时会报错

###Slime文档
[戳这里](http://slime-user-manual-cn.readthedocs.org/en/latest/chapter-1.html)

###Slime配置
文档中有详细的配置说明,不赘述. 这里说一下我遇到的问题.

	; slime setup
	(setq inferior-lisp-program "/usr/local/Cellar/sbcl/1.1.18/bin/sbcl")
	(add-to-list 'load-path "~/.emacs.d/slime/")
	(require 'slime)
	(slime-setup)

注意inferior-lisp-program指向的sbcl必须是可执行文件.我一开始配置为sbcl的安装目录, 结果启动emacs时会报错"xxxx是目录".

配置完成后, 在emacs中输入M-x slime启动.
如果想打开lisp文件时自动加载slime, 输入以下配置:

	; auto load slime when open a lisp
	(add-hook 'slime-mode-hook
		(lambda ()
            (unless (slime-connected-p)
              (save-excursion (slime)))))





