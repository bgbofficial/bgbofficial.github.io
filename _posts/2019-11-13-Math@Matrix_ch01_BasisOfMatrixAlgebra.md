---
layout: post
title: Math@Matrix_ch01_BasisOfMatrixAlgebra
date: 2019-11-13
tag: Math
mathjax: true
---

# Chapter_01 Basis Of Matrix Algebra

## 1.1 矩阵的基本运算

### 1.1.1 矩阵和向量

线性方程组，行向量，列向量。

向量：物理向量（速度、加速度等），几何向量（有向几何箭头），代数向量（代数表示）。

代数向量：常数向量，函数向量，随机向量。

对角线：主对角线，次对角线。

特殊向量：零向量，基本向量。

### 1.1.2 矩阵的基本运算

基本运算：转置 $A^{\mathrm{T}}$，共轭 $A^{\mathrm{*}}$，共轭转置（Hermitian） $A^{\mathrm{H}}$，加法，乘法。

共轭与转置关系： $A^{\mathrm{H}} = (A^{\mathrm{*}})^{\mathrm{T}} = (A^{\mathrm{T}})^{\mathrm{*}}$

共轭：

$$
\mathrm{if}\: A = \begin{bmatrix}
3+i & 5\\
2-2i & i
\end{bmatrix} \mathrm{,then}\:A^{*}=\begin{bmatrix}
3-i & 5\\
2+2i & -i
\end{bmatrix}
$$

乘法：矩阵与标量乘法，（推广到）矩阵与向量的乘法，（推广到）矩阵与矩阵的乘法，乘法结合律，乘法左分配率，乘法右分配率，不满足交换律，（一般不满足）乘法交换律 $AB \ne BA$。

特殊矩阵：逆矩阵，共轭-转置-共轭转置-逆矩阵的关系，幂等矩阵，幂零矩阵，零矩阵。

`矩阵函数`：函数矩阵函数求解 [Link]( https://blog.csdn.net/weixin_39749553/article/details/78835182 ) ，See in Supplementary Notes: [FunctionalMatrix](./2019-11-13-Math@Matrix_SupplementaryNotes01_FunctionalMatrix.md) 。

三角函数：定义，

$$
\begin{align}
&\sin(A)=\sum_{n=0}^{\infty}\dfrac{(-1)^nA^{2n+1}}{(2n+1)!}=A-\dfrac{1}{3!}A^3+\dfrac{1}{5!}A^5-\dotsb\tag{1.1.17}\\
&\cos(A)=\sum_{n=0}^{\infty}\dfrac{(-1)^nA^{2n+1}}{(2n)!}=I-\dfrac{1}{2!}A^2+\dfrac{1}{4!}A^4-\dotsb\tag{1.1.18}\\
&\mathrm{e}^A=\sum_{n=0}^{\infty}\dfrac{1}{n!}A^n=I+A+\dfrac{1}{2}A^2+\dfrac{1}{3!}A^3+\dotsb\tag{1.1.19}\\

\end{align}
$$

矩阵导数：若矩阵 $A$ 的元素 $a_{ij}$ 都是参数 $t$ 的函数，则矩阵的导数定义为

$$
\dfrac{\mathrm{d}A}{\mathrm{d}t}=\dot A = 
$$

矩阵积分：



# Reference

[1*] 张贤达, *矩阵分析与应用（第2版）*. 清华大学出版社.