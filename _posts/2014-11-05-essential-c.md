---
layout: post
title: "essential c++"
description: ""
category: 
tags: []
---
{% include JB/setup %}

#面向对象编程风格

##如何写函数

* pointer和reference的差异
>pointer可能为空,需要确认其值非0.
>reference必定会代表某个对象. 但除非希望在函数内改变参数值, 否则不建议使用reference

* extent和scope
>extent是为对象配置的内存
>scope是对象在程序内的存活区域. 比如函数内对象拥有local scope.

