---
layout: post
post_title: "笔记：Git Essential Training"
post_name: Git-Essential-Training-Notes
post_date: 2015-04-07 08:56
tags: [笔记,数据科学]
published: true
categories: 编程
---
# 课程简介

1. 这些视频是为了增加和补充课堂和教材中的内容。有时候教材太过厚实，习题也太过繁杂，这很容易让你迷失关键和重点。
2. 第一部分总共有5个视频，“总览”可以很好地形容这部分视频。第二部分有12个视频，论及微分学剩下的部分。
3. 很多学数学或是微积分的人，不管是在高中，还是大学，他们只是简单想了解一下重点，这就是本课程的核心。这些视频不需要任何先修课程，任何人都能观看，哪怕你完全不知微积分为何物。

# 第1课 微积分总览
1. 微积分是函数一（微分函数）和函数二（积分函数）之间的桥梁，不过是关于两函数之间关系的学科。微积分作用是知道函数一，求函数二或知道函数二，求函数一。两个函数包含的信息的相同的，从而微积分分为微分学和积分学。
	- differential calculus: find function2 from function1, or find speed from distance
	- integral calculus: find function 1 from function 2,find distance from speed
	- integrate function 2 to find function 1 : integral calculus use speed to find distance
2. function 1 graph tell you the area under function 2，这个可以从f’(s0)=s(t0)=at 来推出
3. 如果function 1 y是height，那么function 2 的s就是rate of change，横坐标都是时间，那么假设人一出生就是20inches,设时间为t，初始速度为 s=0，加速度为 a，距离为 f，求在时间 t 时的距离 f 的值。

		解：

		在时间为 0 时，速度 s0=0+0∗a
		在时间为 t 时，速度 st=0+t∗a
		∵距离 f 为时间 0 到时间 t 所有速度的总和
		即 f=(s0+st)∗t/2
		∴f=at2/2

# 第2课 导数总览
1. 导数其实在求在一段时间内的平均速度

2. 微积分中三个重要的函数：

	- 幕函数 (y = xn) 其导数为 dy/dx=nxn−1
	- 三角函数 (y = sin x) 其导数为 dy/dx=cosx
	- 指数函数 (y = ex) 其导数为 dy/dx=ex

3. 平均斜率 = y变化量/x变化量 = △y/△x

4. 求最低点是微积分的一个主要应用。通过斜率为0，可以求出最低点，即最低点的斜率为0。

		求 y = x2 的导数。

		解：

		∵ dy/dx = 极小下的△y/△x

		即在极小情况下

		△x = 0

		∴ y = x2 的导数为2x

# 第 3 课 极值和二阶导数
distance f(t)， speed = df/dt acceleration d2f/dt2
二阶导数求极值
二阶导数：导数的导数（The Second Derivative The derivative of the derivative）
二阶导数的例子（Examples of Second Derivatives）
凸函数和凹函数（Convex and Concave Curves）
寻找极值点和拐点（Locating the Maximum and Minimum and the Infection Point）
应用：上班的最短时间（求最小值）（Application: Driving to Work Finding the Minimum time）
国外统一定义 f″>0 为凸 convex，表示向上弯曲；相对的凹为 f″<0 concave

极大极小值就是一阶导数为0的点

拐点（inflection point）是弯曲的方向发生了变化，二阶导数在这一点变号。它就是二阶导数为0的点（Inflecion Point: Where the second derivative is zero），即 y″=0 下x的值。

以自己家到MIT的距离，问题是什么地方进入高速，这样会最快的进入MIT 

链式法则（chain rule）,对于求复合函数的导数来说相当有用。以后会有关于链式法则的讨论。

# 第4课 指数函数 
指数函数的倒数还是指数函数
指数函数的另外一个性质：e的x次方乘以e的x次方等于e的2x次方
Ex= 1+x+x2/2！+x3/3!+xn/n!

指数函数是不会无穷大的，因为越到后面导数越小，基本趋近于0
E= 1+1+1/2+1/6……+1/n!这个数在2.5和3之间

举例银行按月计算利息比按年好，如果把计算利息的周期算成n，那么计算总收入就是e的x次方的函数了
n times per year give (1+1/n)n and this approach the magic number e

http://www.ruanyifeng.com/blog/2011/07/mathematical_constant_e.html


链式法则（chain rule）,对于求复合函数的导数来说相当有用。以后会有关于链式法则的讨论。

# 第5课 积分总览

Plan B：integral= function 1 = area under graph
function 1 is the area of function 2

# 第6课 Sin Cos的导数
1. 证明Sinx的导数趋近1（正弦函数的图像是从单位圆推导出来的）
		在三角形中，a2+b2=c2
		两边同时除以c2
		那么cosx2+sinx2=1
2. 如何表示对应圆角度的弧长，因为360就是2π
3. 证明sinx当x=0的时候，导数等于1，但是sinx<x
	这一点可以直接在圆形里头嵌套一个三角形来证明，sinx就是三角形x内角的对边，x就是弧长

4. tanx>x,当0<x<π/2，也就是sinx/x>cosx，在图形上也就是sixx的导数永远在cos上面
	利用弧长公式，构建三角形，使得三角形的面积大于构建的扇形面积来推导（L为弧长，R为扇形半径）
5.sinx的导数是cosx，cosx的导数是-sinx

# 第7课 乘法法则和除法法则
1. ![乘法法则](http://upload.wikimedia.org/math/9/1/3/913a40fea61f096e3188d72fccb772ac.png)
2. 假设原函数为![除法函数](http://upload.wikimedia.org/math/8/5/c/85c4e200964ebf85acaee18f2c1f03f3.png)，那么求导公式为![除法法则](http://upload.wikimedia.org/math/1/5/3/153f55aeaa4bba005e1218e1b7e84f22.png)，口诀：下乘上导-上乘下导，除以下的平方
3. 乘法法则适用于任何的正数
4. 推导乘法法则是如何来的：利用的几何的方法来推导
5. 推导除法法则：利用乘法法则来推导
6. 最后利用除法法则来计算x的-n次幂，证明幂函数的求导法则同样适用于负数

# 第8课 复合函数和链式法则

1. 利用三角函数 \\(y=\sin{3x}\\) 的图像求解这个符合函数
2. 求解 \\(z=e^{{-x^2}/2}\\) 得出一个偶函数的曲线 bells shaped curve，这个曲线对于研究概率非常重要，而z的导数\\(z\prime=-xe^((-x^2)/2)\\)确实一个奇函数
3. 对上面的函数做二次求导，\\(z\prime\prime=(x^2-1)e^((-x^2)/2)\\)，

# 第9课 极限和连续函数


<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>
