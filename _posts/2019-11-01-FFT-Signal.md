---
layout: post
title: 数字图像分析@基础二 *Signal-1D Fourier Alysis*
date: 2019-11-01 
tag: math, signal
mathjax: true
---

# Chapter3 Fourier Transform

## 3.2 周期信号的傅里叶级数分析

### （一）三角函数形式的傅里叶级数

$\qquad$由数学分析课程已知，周期函数 $f(t)$ 可由三角函数的线性组合来表示，若 $f(t)$ 的周期为 $T_1$，角频率为 $\omega=\dfrac{2\pi}{T_1}$，频率$f_1=\dfrac{1}{T_1}$，傅里叶级数展开表达式为

$$\begin{aligned}
f(t) 
&=\quad a_0 +a_1\cos{(\omega_1t})+b_1\sin{(\omega_1t})+a_2\cos{(\omega_2t}) +\\[2ex]
& \qquad\,\, b_2\sin{(\omega_2t})+ \dotsb + a_n\cos{(\omega_1t})+b_n\sin{(\omega_1t})+\dotsb\\
&=\quad a_0+\sum_{n=1}^{\infty}[a_n\cos{(n\omega_1t)+b_n\sin{(n\omega_1t})}]
\end{aligned}\tag{3-1}$$

其中 $n$ 为正整数，各个谐波成分的幅度值按下各式计算：  
$\qquad$直流分量

$$a_0 = \dfrac{1}{T_1}\int_{t_0}^{t_0+T_1}f(t) \mathrm{d}{t}\tag{3-2}$$

$\qquad$余弦分量的幅度

$$a_n = \dfrac{2}{T_1}\int_{t_0}^{t_0+T_1}f(t)  \cos{(n \omega_1 t)}\, \mathrm{d}{t}\tag{3-3}$$

$\qquad$正弦分量的幅度

$$b_n = \dfrac{2}{T_1}\int_{t_0}^{t_0+T_1}f(t)  \sin{(n \omega_1 t)}\, \mathrm{d}{t}\tag{3-4}$$

其中 $n=1,2,\dotsb$。

将式（3-1）中同频率项加以合并，可以写成另一种形式

$$f(t) = c_0 +\sum_{n=1}^{\infty} c_n\cos{(n\omega_1t+ \varphi_n)}\tag{3-5}$$
或

$$f(t) = d_0 +\sum_{n=1}^{\infty} d_n\sin{(n\omega_1t + \theta_n)}$$
比较（3-1）和（3-5）得出变量关系

$$\left.\begin{aligned}
& a_0 = c_0 = d_0 \\[2ex]
& c_n = d_n =  \sqrt{a_n^2 + b_n^2} \\[2ex]
& a_n = c_n \cos\varphi_n = d_n \sin\theta_n \\[2ex]
& b_n = -c_n\sin \varphi_n = d_n\cos \theta_n \\[2ex]
& \tan \theta_n = \dfrac{a_n}{b_n} \\[2ex]
& \tan \theta_n = - \dfrac{b_n}{a_n} \\[2ex]
& (n=1,2,\dotsb)
\end{aligned}\right\}\tag{3-6}$$

$\qquad$各个正、余弦分量的频率 $(n=1,2,\dotsb)$ 必定是基频 $f_1(f_1=1/T_1)$ 的整数倍 $(f_1,2f_1,3f_1,\dotsb)$。  
$\qquad$从式子（3-3）到（3-6）看出，各个分量幅值 $a_n,b_n,c_n$ 及相位 $\varphi_n$ 都是 $n\omega_1$ 的函数。可以把 $c_n-n\omega_1$ 和 各分量的相位 $\varphi_n-n\omega_1$ 关系图画出，分别得到幅度频谱和相位频谱。  

![3-1](/images\posts\markdown\2019-11-01-FFT-Signal\3-1.png)  
$\qquad$周期信号频谱只会出现在 $0,\omega_1,\omega_2,\dotsb$ 离散谱上。

### （二）指数形式的傅里叶级数
$\qquad$将周期信号的傅里叶级数表示成指数形式，已知

$$ f(t)=a_0+\sum_{n=1}^{\infty}[a_n\cos{(n\omega_1t)+b_n\sin{(n\omega_1t})}]\tag{3-1}$$
根据欧拉公式

$$\begin{aligned} &\cos{(n\omega_1t)}=\dfrac{1}{2}(e^{\mathrm{j}{nw_1t}}+e^{\mathrm{-j}{nw_1t}})\\[2ex] & \sin{(n\omega_1t)}=\dfrac{1}{2\mathrm{j}}(e^{\mathrm{j}{nw_1t}}-e^{\mathrm{-j}{nw_1t}})\end{aligned}$$





# Reference
[1] 郑君里, 应启珩, and 杨为理, 信号与系统(上册). 高等教育出版社, 2000.  
[2] 谷超豪等, 数学物理方程. 高等教育出版社, 2002.
