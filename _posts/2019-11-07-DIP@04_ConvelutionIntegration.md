---
layout: post
title: 数字图像分析@04 *Convelution Integration*
date: 2019-11-04 
tag: math, signal
mathjax: true
---


#  § Convelution Integration

## 1.信号的时域分解

`主要内容`：任意信号时域分解的方法

`基本要求`：了解时域分解公式的含义

`卷积积分作用`

信号处理的重头到位的三个关键问题：（1）基本信号及其响应；（2）任意信号分解；（3）LTI系统分析（即求任意信号的响应）。

卷积积分的作用是分解 $f(t)$ 为基本信号的线性组合。

*TYPORA tips*: 

- 中文输入法，且有公式的情况下，公式结尾处按`crtl+enter`会空一行出来；:x:
- `shift+enter`可以增加一个空行；:x:

### （1）预备知识

![image-20191107190344173](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191107070335.png)

问题？ $f_1(t)=?p(t)$ 即，$f_1(t)$ 等于多少个 $p(t)$ ，其中 $p(t)$ 是单位矩形脉冲。直观看出：

$$
f_1(t)=\dfrac{\mathrm{A}}{^1/_\Delta}=\mathrm{A}\Delta p(t)
$$

### （2）任意信号分解

问：怎么将 $f(t)$ 用单位矩形脉冲进行时域分解？

![image-20191107193307048](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191107073256.png)

答：$f(t)$ 可以将其表示成多个单位矩形脉冲相加而成的函数 $\hat f(t)$。

- “0”号脉冲高度 $f(0)$ ，宽度为 $\Delta$，用 $p(t)$ 表示为：$f(0)\Delta p(t)$；
- “1”号脉冲高度 $f(\Delta)$ ，宽度为 $\Delta$，用 $p(t)$ 表示为：$f(\Delta) \cdot \Delta \cdot p(t-\Delta)$；
- “-1”号脉冲高度 $f(-\Delta)$ ，宽度为 $\Delta$，用 $p(t)$ 表示为：$f(-\Delta) \cdot \Delta \cdot p(t+\Delta)$；。如下图

![image-20191107193224328](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191107073219.png)

总结，可以写出

$$
\hat f(t)=\sum_{n=-\infty}^{\infty}f(n\Delta)\Delta p(t-n\Delta)
$$

当 $\Delta \to 0$ 时，

$$
\left\{\begin{aligned}
& \Delta \to \mathrm{d}{\tau},\:n\Delta \to \tau,\:\sum \to \int\\
& p(t-n\Delta) \to \delta(t-\tau)
\end{aligned}\right.
$$

得到：

$$
\lim_{\Delta \to 0}\hat f(0) = f(t) = \int_{-\infty}^{+\infty}f(\tau)\delta(t-\tau)\mathrm{d}{\tau}
$$

一般地，有：

$$
y_+(t)=\int_{-\infty}^{+\infty}f_1(t) \cdot f_2(t- \tau)\mathrm{d}{\tau} =f_1(t) \ast f_2(t)
$$

其中 $y_+(t)$ 是响应。
