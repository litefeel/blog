---
layout: post
post_title: "笔记：Calculus One"
post_date: 2015-05-10 20:19
post_name: note-of-calculus-one
tags: [笔记,数据科学]published: true
categories: 编程
---

学习这门课乐趣无穷，每一个章节都被切分为平均不到3分钟的小视频，加上动感俏皮的片头音乐，每次一个视频结束都会有新的学习新鲜感，这种学习模式的驱动力是其他课程无法比拟的。更重要的是，这门课把微积分讲的非常的直观，我想任何有点高中数学基础的人完全可以听得明明白白，即便是文科。
学习感想用下面公式表示： $\frac{d快乐}{d学习}>0 $
此文档中更新中……

## 1. Welcome to Calculus One
### 1.1 Introduction To Calculus One
1. Why is calculus going to be so much fun：现在很多导论型的课程都会在第一节课告诉学生，类似“未来学习的主题课程非常的简单，学习过程非常的有趣，跟你以前的体验绝对不一样，无论你是什么基础，你要你跟着我就都可以学会”的话，这一小节也起来的类似的作用。
2. How is this course structured：这门课程任何时候都开放，是一门自学型的Mooc课程。

## 2. Functions and Limits
### 2.1 Introduction
1. How do we get started with calculus：微积分是一门关系的学问，是输入变量与输出变量之间的关系，比如你把一个苹果（输入变量）放进榨汁机（函数）最终获得苹果汁，这样一种关系；其次我们还会讨论极限的概念。
### 2.2 Functions? What's a Function?
1. What is a function?
    - 函数是一个很简单的概念，Function就是函数，比如$f(x)=\sin x$，或者$f(x)=2x+7$；
    - 真实世界的函数比如你在Google中搜索578，那么gogole会给出57890000的搜索结果页面，其中你的搜索词就是函数中的输入变量（input）,57890000就是Google这个函数中的输入变量(ouput);
2. When are two functions the same?
    -  $f(x)=(1+x)^2$与$g(x)=x^2=2x+1$是相等的;
    -  $f(x)=\frac{x^2}{x}$与$g(x)=x$是不相等的,因为这里前者的x不可以等于0;
3. How can more functions be made?
    - 举例说明复合函数的概念来构建新的函数,比如$f(x)=2x+1$,$g(x)=x^2$来构建一个新函数$f(g(x))$
    
### 2.3 Functions in the Real World
1. What are some real-world examples of functions? 
    - 摄氏度与华氏度之间的转换函数：$f(x)=\frac{9x}{5}+32$  
    - Google 搜索关键字和搜索结果页之间的函数
2. What is the domain of square root?
    - $\sqrt x $的定义域是 $x\geq 0$
    
### 2.4 Limits? What's a Limit?
1. Morally, what is the limit of a sum? 
    -** 极限和**：The limit of sum is the sum of the limits provided the limits exist
    - 也就是两个函数和的极限就是两个函数极限值相加：$\lim_{x \to a}(f(x)+g(x))=\lim_{x \to a}f(x)+\lim_{x \to a}g(x)$
2. What is the limit of sin (1/x)? 
    - **极限的定义**：To say $\lim_{x \to a}=L$ means f(x) can be made as close to L as desired by making x close enough to a；
   - $\lim_{x \to 0} \sin (\frac {\pi}{x}) $不存在（DNE），因为x取不同的小值趋向的值都不同
    - 比如第一组：0.1/0.01/0.001/……：有正有负
    - 比如第二组：0.75/0.075/0.0075/…… : 趋向于$-\frac {\sqrt x}{2} $
    - 比如第三组：0.7/0.07/0.007/……：有正有负
3. What is the limit of (sin x)/x?  
    - $\lim_{x \to 0} (\frac{\sin x}{x})=1$
    - **夹逼定理(Squeeze Theorem)** ：$g(x)\leq f(x) \leq h(x)$, x near a,  $\lim_{x \to a }g(x)= \lim_{x \to a}h(x)=L $, Then $ \lim_{x \to a} f(x)=L$
    - 用三个函数图像在x=a点向粘合来直观感受这个定理
    - Eg.: $\cos x <\lim_{x \to 0} (\frac{\sin x}{x}) < 1$，根据夹逼定理可以推导出$\lim_{x \to 0} (\frac{\sin x}{x})=1$
4. What is the limit of (x^2 - 1)/(x-1)?
    - 极限值为2，因为当x趋进1时，x-1的值仍然不为零，所以等式可以约去，$ \lim_{x \to 1} \frac {x^2-1}{x-1}$

### 2.5 Working with Limits
1. What is the limit of a product? 
    - **极限积**：The limit of product is the product of the limits provided the limits exist
2. What is the limit of a quotient? 
    - **极限商**：The limit of division is the division of the limits provided the limits exist3 and the Denominators is not equal to Zero

### 2.6 Limits in Motion
1. How fast does a ball move：利用向下丢一个球所走的路程（上下都算）和所用的时间，绘制出这个球时间与路程的函数图像，强调的概念就是球向下时，受到重力的影响，速度越来越快，但是击中地面之后球反向向上运动，受到重力的阻力作用，速度运来越来越慢，直到为0，然后又掉下地面，这样一个过程的图像。这个小结是为之后学习瞬时速度做铺垫，也就是积分的概念。

## 3. The End of Limits
### 3.1 Introduction
1. What else is there to study about functions and limits:简单提及接下来即将要学习的主题。
### 3.2 Continuity
1. What is a one-sided limit? 
    - 从右趋近：$\lim_{x \to a^+} f(x)=L$ means that f(x) is as close as you want to L provided x is near enough a from the right
    - 从左趋近：$\lim_{x \to a^-} f(x)=L$ means that f(x) is as close as you want to L provided x is near enough a from the left
    - 极限不存在的定义：if $\lim_{x \to a^+} f(x) \not= \lim_{x \to a^-} f(x)$, then $\lim_{x \to a} f(x)$ DNE 
2. What does "continuous" mean?
    - to say "f(x) is continuous at a" means that $\lim_{x \to a}f(x)=f(a)$
    - nearby input give nearby output
    - 可以利用连续的性质构建函数推倒$\sqrt 2$的范围
3. What is the intermediate value theorem? 
    - **the intermediate value theorem**： if  function f is continuous with an interval [a, b]， and y is between f(a) and f(b), then there is an x between a and b so that f(x)=y
4. How can I approximate root two? 
    - 利用intermediate value theorem，构建$f(x)=x^2-2$，不断地代入值找到f(x)=0的区间

### 3.3 Infinity? How can I work with that?
1. Why is there an x so that f(x) = x?
2. What does lim f(x) = infinity mean? 
3. What is the limit f(x) as x approaches infinity?
4. Why is infinity not a number? 

### 3.4 Slope?
1. What is the difference between potential and actual infinity? 
2. What is the slope of a staircase? 
3. How fast does water drip from a faucet?