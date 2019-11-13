---
layout: post
title: Math@Matrix_SupplementaryNotes01_FunctionalMatrix
tag: Math
mathjax: true
---

# Matrix_01 Supplementary Notes 01: Functional Matrix

## 1. 问题的提出

$$
\cos \begin{bmatrix}
-2 & 3 \\
-6 & 7
\end{bmatrix} = \:?
$$

## 2. Jordan标准型

## 2.1 引言

“对角标准型”是线性代数中的概念，“Jordan”标准型是矩阵分析中的概念。“对角标准型”是“Jordan标准型”的特例。能化成“对角标准型”的 $n$ 阶矩阵称为“单纯阵”。不是所有的 $n$ 阶方阵都能化为“对角标准型”，但是所有 $n$ 阶方阵能化成“Jordan”标准型。《矩阵分析》中一个重要的研究点就是 $n$ 阶方案的标准化问题。

一个n阶方阵能够对角化：每一个特征值的代数重复度和几何重复度均相等。称为“单纯矩阵”。

设 $\lambda_1,\lambda_2,\dotsb,\lambda_k$ 是 $n$ 阶方阵 $A$ 的 $k$ 个相异特征值，其重数分别为 $r_1,r_2,\dotsb,r_k$，则称 $r_i$ 是矩阵 $A$ 的特征值 $\lambda_i$ 的代数重复度，对用特征值的解空间 $V_{\lambda_i}$ 的维数称为 $A$ 的特征值 $\lambda_i$ 的几何重复度。若A的每个特征值的代数重复度与几何重复度相等，则称A为单纯矩阵。几何重复度不大于它的代数重复度。 

举例1：

$$
A=\begin{pmatrix}
3 & -1 & -2 \\
2 & 0 & -2 \\
2 & -1 & -1
\end{pmatrix}
$$

特征值 $\lambda$，代数重复度 $m$ 和几何重复度 $a$ 分别为：

$$
\lambda_1=0,m_1=1,a_1=1 \\
\lambda_2=\lambda_3=1,m_1=2,a_2=2
$$

所以，每个特征值的代数重复度和几何重复度相等。可化为对角矩阵，

$$
\begin{pmatrix}
0 &  &  \\
 & 1 &  \\
 &  & 1
\end{pmatrix}
$$

粒子2：

$$
B=\begin{pmatrix}
3 & 2 & -2 \\
-1 & -1 & 1 \\
4 & 2 & -3
\end{pmatrix}
$$

特征值 $\lambda$，代数重复度 $m$ 和几何重复度 $a$ 分别为：

$$
\lambda_1=1,m_1=1,a_1=1 \\
\lambda_2=\lambda_3=1,m_1=2,a_2=1
$$

所以，每个特征值的代数重复度和几何重复度不相等。可化为Jodan标准型，

$$
\begin{pmatrix}
0 &  &  \\
 & -1 & 1 \\
 &  & -1
\end{pmatrix}
$$

### 2.2 多项式 $^{[2]}$ 

定义：已知， $A \in C^{ n\times n}$ 和关于变量 $x$ 的多项式

$$
f(x) = a_nx^n+a_{n-1}x^{n-1}+\dotsb+a_{1}x^{1}+a_0
$$

那么，称

$$
f(A) = a_nA^n+a_{n-1}A^{n-1}+\dotsb+a_{1}A^{1}+a_0I
$$

是 $A$ 的矩阵多项式。

设 $A$ 是一个 $n$ 阶矩阵，$J$ 为其 Jordan 标准型，则

$$
\begin{aligned} A & =PJP^{-1}\\
&=P\mathrm{diag}(J_1,J_2,\dotsb,J_r)P^{-1}\\
& =P\mathrm{diag}(J_1(\lambda_1),J_2(\lambda_2),\dotsb,J_r(\lambda_r))P^{-1}\\
\end{aligned}
$$

于是有

$$
f(A)=P\mathrm{diag}(J_1(\lambda_1),J_2(\lambda_2),\dotsb,J_r(\lambda_r))P^{-1}
$$

称上面的表达式为`矩阵多项式` $f(A)$ 的 `Jordan表示`。其中

$$
J_i(\lambda_i)= {\begin{bmatrix}
\lambda_i & 1 &  & \\
 & \lambda_i & \ddots & \\
 & & \ddots &1 \\
 &&& \lambda_i
\end{bmatrix}}_{d_i \times d_i} (i=1,2,\dotsb,r)
$$

$$
J_i^k(\lambda_i)= {\begin{bmatrix}
\lambda_i^k & c_k^1 \lambda_i^{k-1} & \cdots   & c_k^{d_i-1} \lambda_i^{k-d_i-1} \\
 & \lambda_i^k & \ddots & \vdots \\
 & & \ddots & c_k^1 \lambda_i^{k-1} \\
 &&& \lambda_i^k
\end{bmatrix}}_{d_i \times d_i} (i=1,2,\dotsb,r)
$$

$$
f(J_i)= {\begin{bmatrix}
f(\lambda_i) & f'(\lambda_i) & \cdots  & \dfrac{1}{(d_i-1)!}f^{d_i-1}(\lambda_i)\\
 & f(\lambda_i) & \ddots & \vdots\\
 & & \ddots & f'(\lambda_i) \\
 &&& f(\lambda_i)
\end{bmatrix}}_{d_i \times d_i} (i=1,2,\dotsb,r)
$$

🌰1：已知多项式

$$
f(x)=x^4-2x^3+x-1
$$

与矩阵

$$
A=\begin{bmatrix}
3 & 0 & 8 \\
3 & -1 & 6 \\
-2 & 0 & -5
\end{bmatrix}
$$

求 $f(A)$。




# 其他问题

函数 $f(x)'=(x^2)'=2x$，那么 $f(x)^{i}=?$ 也就是 Imaginary derivative of $x$；$f(x)^{'1/2}=?$ ，也就是 Half Derivative of $x$，即分数阶微分。 

# Reference

[2] [百度文库课件：矩阵函数]( https://wenku.baidu.com/view/91043fc74028915f804dc241.html?sxts=1573650251601 )