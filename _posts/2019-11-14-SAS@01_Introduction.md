---
layout: post
title: SAS@01_Introduction
tag: Signal
mathjax: true
---

# Signal and system@01_Introduction

电容电流公式

$$
i = C\dfrac{\mathrm{d}v_C(t)}{\mathrm{d}t}
$$

电感电压公式

$$
u_L(t)=L\dfrac{\mathrm{d}}{\mathrm{d}t}i_L(t)
$$

$RCL$ 串联回路，激励是电压源 $e(t)$ ，求电流 $i(t)$，如图：

![RLC](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191115103838.png)

由元件的理想特性与 KVL（$u_e=u_R+u_L+u_c$） 可建立微分方程组：

$$
\begin{aligned}
& i=i_R=i_L=i_C=C\dfrac{\mathrm{d}u_C}{\mathrm{d}{t}}\\
& u_R=R\cdot i=R\cdot C\dfrac{\mathrm{d}u_C}{\mathrm{d}{t}},\:
u_L=L\dfrac{\mathrm{d}i_L}{\mathrm{d}t}=LC\dfrac{\mathrm{d}^2u_C}{\mathrm{d}t^2}\\
& \mathrm{KVL:}\:u_C+u_L+u_R=e\\
& 1.\,i(t)(\mathrm{variable}):\dfrac{1}{C}\int_{-\infty}^t i\mathrm{d}{t} + L\dfrac{\mathrm{d}i}{\mathrm{d}t}+iR=e\quad(\mathrm{Differentiate\,both\,sides})\\
& \implies LC\dfrac{\mathrm{d}^2i}{\mathrm{d}t^2}+RC\dfrac{\mathrm{d}i}{\mathrm{d}t}+i=C\dfrac{\mathrm{d}e}{\mathrm{d}t}\\
& 2.\,u_C(\mathrm{variable}):\:u_C+LC\dfrac{\mathrm{d}^2{u_C}}{\mathrm{d}t^2}+RC\dfrac{\mathrm{d}u_C}{\mathrm{d}t}=e\\
& \implies LC\dfrac{\mathrm{d}^2u_C}{\mathrm{d}t^2}+RC\dfrac{\mathrm{d}u_C}{\mathrm{d}t}+u_C=e(t)\\ 
\end{aligned}
$$

节约；

$$
out=\mathrm{mean}(Y-X\cdot W)=\mathrm{mean}
\left\{
\begin{bmatrix} 
1 & 2  \\
10 & 11 \end{bmatrix}-\begin{bmatrix} 2&3&4\\4&5&6\end{bmatrix}\cdot
\begin{bmatrix} 1&3\\2&4\\3&5\end{bmatrix}
\right\}
$$

$$
out = \mathrm{mean}(Y-X\cdot W)=\frac{1}{4}\{[y_{11}-(x_{11}w_{11}+x_{12}w_{21}+x_{13}w_{31})]
+\dotsb\}
$$

