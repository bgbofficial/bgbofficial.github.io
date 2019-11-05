---
layout: post
title: 数字图像分析@基础三 *Practice FT*
date: 2019-11-04 
tag: math, signal
mathjax: true
---

# DFT
对于一个长度为 $N$ 的离散信号 $x(n)$，取值范围为 $0 \le n \le N-1$，其离散傅里叶变换（DFT）定义为：

$$\boldsymbol{X}(k)=\sum_{n=0}^{N-1}x(n)\mathrm{e}^{-\mathrm{j}\frac{2\pi}{N}kn}=\sum_{n=0}^{N-1}x(n)\boldsymbol{W}_N^{kn}\tag{5.1}$$
其中， $\boldsymbol{W}_N^{kn}=\mathrm{e}^{-\mathrm{j}\frac{2\pi}{N}}$，$k$ 的取值范围为 $0 \le k \le N-1$。简记为

$$\boldsymbol{X}(k)=\mathrm{DFT}[x(n)]\tag{5.2}$$

$$ \\[2ex]x(n) \stackrel{\mathrm{DFT}}{\longrightarrow}\boldsymbol{X}(k) \tag{5.3}$$

$$ \\[2ex] x(n)=\dfrac{1}{N}\sum_{k=0}^{N-1} \boldsymbol{X}(k)\mathrm{e}^{-\mathrm{j}\frac{2\pi}{N}kn}=\dfrac{1}{N}\sum_{k=0}^{N-1} \boldsymbol{X}(k)\boldsymbol{W}_N^{-kn}\tag{5.4}$$