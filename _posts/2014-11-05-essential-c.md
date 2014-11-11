---
layout: post
title: "essential c++"
description: ""
category: 
tags: []
---
{% include JB/setup %}
##C++基础

1. 基础数据型别
2. 算术运算符,逻辑运算符,关联运算符
3. 条件及分支以及循环控制语句
4. 复合型别(如指针和 数组)
5. 标准的,通用的抽象化程序库

> So, 这些是语言教程的一般流程


##面向过程编程风格

###如何写函数

1. **pointer和reference的差异:**

	* pointer可能为空,需要确认其值非0.
	*  reference必定会代表某个对象. 但除非希望在函数内改变参数值, 否则不建议使用reference.
	
2. **extent和scope的差异:**

	*  extent是为对象配置的内存.
	*  scope是对象在程序内的存活区域. 比如函数内对象拥有local scope.

3. **动态内存/堆内存:**

	*  由程序员自行管理. 通过new分配, 通过delete释放(无需检查指针是否为0).

4. **如果为参数提供了默认值, 将默认值置于函数声明处.**

5. **使用局部静态对象, 而非定义在file scope中**

	*  *它们区别是?*

6. **使用inline函数**

	*  最好声明在头文件中

7. **重载函数**

	*  参数表不相同的函数可以拥有相同的函数名称

8. **模板函数**

	*  template <typename elemType>
	*  *使用时怎样获取具体typename?*

9. **函数指针**

		const vector<int>* (* fun_pointer)(int);
		fun_pointer = fun_name;
	   
10. **头文件只写声明不写定义, inline函数是例外**

11. **const 的声明以及extern**
	*  *没完全搞明白, 待补充*
	
	
	
##泛型编程风格

1. 创建通用的工具以去除冗余
2. 实现通用接口以减少耦合



##基于对象的编程风格

###如何实现一个class

1. 抽象化. 确定希望实行于class之上的行为和存放的元素.
2. 写class定义式.
	*  public和private用来标示每个区段的"members存取权限".
	*  public:任何地方被取用.
	*  private:只能在member function内被取用或者在'class friend内被取用'

3. 所有声明必须在主体内, 定义则不一定
	*  定义在主体内的function自动被视为inline函数



##面向对象的编程风格

##以template进行编程

##异常处理




























