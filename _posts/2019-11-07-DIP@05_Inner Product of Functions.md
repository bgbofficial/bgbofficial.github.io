---
layout: post
title: 数字图像分析@05 *Inner Product of Functions*
date: 2019-11-08 
tag: Signal
mathjax: true
---


#  § Inner Product of Functions

### Vectors

已知：向量 $\boldsymbol{a}=(a_1,\dotsb,a_n)$ 和 向量 $\boldsymbol{b}=(b_1,\dotsb,b_n)$ 垂直（正交），$\iff \sum\limits_{i=1}^{n} a_i b_i=0$。

若函数 $f(x)$ 记为 $\{f(x_1),f(x_2),\dotsb, f(x_n) \mid x_i是[a,b]的n等分中的第i点\}$，故 

$$
\begin{aligned}
& \{f(x_1),f(x_2),\dotsb, f(x_n)\mid n\to \infty \} \\
& \{g(x_1),g(x_2),\dotsb, g(x_n)\mid n\to \infty \} \\
\end{aligned}
$$

若垂直，则 

$$
\iff \lim\limits_{\Delta x_i \to 0} \sum\limits_{i=1}^{n}f(x_i)g(xi)\Delta x_i = \int_a^bf(x)g(x)\mathrm{d}x=0
$$

解释：$[a,b]$ 上的函数定义就是给出 $[a,b]$ 中每个点的 $f(x)$ 值。所以给出 $[a,b]$ 的 $n$ 等分点的 $f$ 值。也就是给出了 $f$ 的部分信息，且当 $n\to\infty$ 时，这些部分信息也就逼近了 $f$ 的全部信息。显然 $n$ 越大时，一个点的 $f$ 值代表的权重越小（只能近似代表 $f$ 在全区间的 $^1/_n$ 段中的信息）。因此，计算两个向量的內积时，两个函数在同一点的函数值相乘后应该再乘以这一点的权重 $=^1/_n$ ，也就是 $[a,b]$ 的宽度 $\Delta x_i$。

#  References

[1] [如何通俗的解释：函数之积的积分可以视为有限维空间中内积概念的推广？如何理解三角函数的系的正交性？](https://www.zhihu.com/question/268621013/answer/716108974)

