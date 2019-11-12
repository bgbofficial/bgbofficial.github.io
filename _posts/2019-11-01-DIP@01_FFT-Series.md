---
layout: post
title: 数字图像分析@01 *Series*
date: 2019-11-01 
tag: Math
mathjax: true
---

# 十二章 无穷级数
## 第一节 常数项级数的概念和性质
### 一、常数项级数的概念
- 数列： $u_1,u_2,u_3,\dotsc,u_n,\dotsc,$ 。
- 级数（常数项无穷级数）：$\sum\limits_{n=1}^{\infty}u_n =u_1+u_2+u_3+\dotsb+u_n+\dotsb,$ 。
- 一般项：$u_n$ 。
- 部分和：$s_n=u_1+u_2+\dotsb+u_n=\sum\limits_{i=1}^{n}u_i$ 。 
- 部分和数列：$\{s_n\}$ 。
- 收敛：如果级数 $\sum\limits_{n=1}^{\infty}u_n$ 的部分和数列 $\{s_n\}$ 有极限，即

$$
\lim_{x \to + \infty}s_n=s,
$$

此时，$s$ 叫级数的和。  
- 余项：$r_n=s-s_n=u_{n+1}+u_{n+2}+\dotsb$ 。
- 误差：余项的绝对值  $\left\lvert r_n \right\rvert$。

### 二、收敛级数的基本性质
- 性质1：如果级数 $\sum\limits_{n=1}^{\infty}u_n$ 收敛于 $s$ ，则级数 $\sum\limits_{n=1}^{\infty}ku_n$ 也收敛，其和为 $ks$ 。
- 性质2：如果级数 $\sum\limits_{n=1}^{\infty}u_n$ 、 $\sum\limits_{n=1}^{\infty}v_n$ 分别收敛于和 $s$ 、 $\sigma$ ，则级数 $\sum\limits_{n=1}^{\infty}(u_n \pm v_n)$ 也收敛，且其和为 $s \pm \sigma$ 。
- 性质3：在级数中去掉、加上或改变有限项，不会改变级数的收敛性。
- 性质4：如果级数 $\sum\limits_{n=1}^{\infty}u_n$ 收敛，则这对级数的项任意加括号后所成的级数

$$
    (u_1+\dotsb+ u_{n_{1}})+(u_{n_{1}+1}+\dotsb+u_{n_{2}})+(u_{n_{k-1}+1}+\dotsb+u_{n_{k}})+\dotsb
$$

仍然收敛，且其和不变。

- 性质5（级数收敛的必要条件）：如果级数 $\sum\limits_{n=1}^{\infty}u_n$ 收敛，则它的一般项 $u_n$ 趋于零，

$$
    \lim_{n \to \infty} u_n = 0.
$$

### 三、柯西审敛原理
判断一个级数的收敛性质。

- 定理（$\color{Brown}{柯西审敛原理}$）：级数 $\sum\limits_{n=1}^{\infty}u_n$ 收敛的充分必要条件为：对于任意给定的正数 $\varepsilon$，总存在正整数 $N$，使得当 $n>N$时，对于任意的正整数 $p$，都有

$$
    \left\lvert u_{n+1}+u_{n+2}+\dotsb+u_{n+p} \right\rvert < \varepsilon 
$$


成立。  
证：$\left\lvert u_{n+1}+u_{n+2}+\dotsb+u_{n+p} \right\rvert=\left\lvert s_{n+p}-s_n \right\rvert$。$\varepsilon-N$ 语言是指的：$\varepsilon$ 是误差，只要想，就能小于给定的误差 $\varepsilon$。

## 第二节 常数项级数的审敛法
### 一、正项级数及其审敛法
许多级数的收敛性问题可以归结为正项级数的收敛性问题。  
级数 $u_1+u_2+\dotsb+u_n+\dotsb$ 是正项级数 ($u_n\ge0$) ，它的部分和为 $s_n$ 。显然，数列 $\{s_n\}$ 是一个单调增加数列。若数列 $\left\lvert s_n \right\rvert$ 有界，根据单调有界必有极限：知级数必收敛于  $\lim\limits_{n \to \infty}s_n=s$ 。
- 定理1：正项级数 $\sum\limits_{n=1}^{\infty}u_n$ 收敛的充分必要条件是：它的部分和数列 $\{s_n\}$ 有界。
- 定理2（$\color{Brown}{比较审敛法}$）：设 $\sum\limits_{n=1}^{\infty}u_n$ 和 $\sum\limits_{n=1}^{\infty}v_n$ 都是正项级数，且 $u_n \le v_n(n=1,2,\dotsc)$ 。若级数 $\sum\limits_{n=1}^{\infty}v_n$ 收敛，则级数 $\sum\limits_{n=1}^{\infty}u_n$ 收敛；反之，若级数 $\sum\limits_{n=1}^{\infty}u_n$ 发散，则级数 $\sum\limits_{n=1}^{\infty}v_n$ 发散。
    - 推论：$u_n \le kv_n(k>0)$
- 定理3（$\color{Brown}{比较审敛法的极限形式}$）：设$\sum\limits_{n=1}^{\infty}u_n$和$\sum\limits_{n=1}^{\infty}v_n$都是正项级数，
    - （1）如果 $\lim\limits_{n \to \infty}{\dfrac{u_n}{v_n}}=l (0 \le l < +\infty)$ ，且级数 $\sum\limits_{n=1}^{\infty}v_n$ 收敛，则级数 $\sum\limits_{n=1}^{\infty}u_n$ 收敛；
    - （2）如果 $\lim\limits_{n \to \infty}{\dfrac{u_n}{v_n}}=l > 0$ 或 $\lim\limits_{n \to \infty}{\dfrac{u_n}{v_n}}=+\infty$ ，且级数 $\sum\limits_{n=1}^{\infty}v_n$ 发散，则级数 $\sum\limits_{n=1}^{\infty}u_n$ 发散。

- 定理4（$\color{Brown}{比值审敛法，达朗贝尔(d'Alembert)判别法}$）：设 $\sum\limits_{n=1}^{\infty}u_n$ 为正项级数，如果

$$
    \lim_{n \to \infty} \dfrac{u_{n+1}}{u_n}= \rho，
$$

则当 $\rho < 1$ 时级数收敛； $\rho>1$ （或 $\lim\limits_{n \to \infty} \dfrac{u_{n+1}}{u_n}= \infty$ ）时级数发散； $\rho=1$ 级数可能收敛可能发散。
- 定理5（$\color{Brown}{根值审敛法，柯西判别法}$）：设 $\sum\limits_{n=1}^{\infty}u_n$ 为正项级数，如果

$$
    \lim_{n \to \infty} \sqrt[n]{u_n} = \rho，
$$

则当 $\rho<1$ 时收敛，  $\rho >1$（或 $\lim\limits_{n \to \infty} \sqrt[n]{u_n}=+ \infty$ ）时级数发散， $\rho=1$ 时级数可能收敛也可能发散。

- 定理6（$\color{Brown}{极限审敛法}$）：设 $\sum\limits_{n=1}^{\infty}u_n$ 为正项级数，
    - （1）如果 $\lim\limits_{n \to \infty}nu_n=l>0$ 或 $\lim\limits_{n \to \infty}nu_n=+\infty$，则级数 $\sum\limits_{n=1}^{\infty}u_n$ 发散；
    - （2）如果 $p>1$，而 $\lim\limits_{n \to \infty} n^p u_n=l (0 \le l < +\infty)$ ，则级数 $\sum\limits_{n=1}^{\infty}u_n$ 收敛。  
    证明：用极限形式的比较审敛法，分别取 $v_n=\dfrac{1}{n}$ 和 $v_n=\dfrac{1}{n^p}$ 。

### 二、交错级数及其审敛法
所谓交错级数：

$$
u_1-u_2+u_3-u_4+\dotsb,
$$

其中 $u_n$ 都是正数。
- 定理7（莱布尼兹定理）：如果交错级数 $\sum\limits_{n=1}^{\infty}(-1)^{n-1} u_n$ 满足条件：  
    （1） $u_n \ge u_{n+1}(n=1,2,3,\dotsc)$ ；  
    （2） $\lim\limits_{n \to \infty} u_n =0$,  
    则级数收敛，且其和 $s \le u_1$ ，其 余项 $r_n$ 的绝对值 $|r_n| \le u_{n+1}$。

### 三、绝对收敛和条件收敛
- 绝对收敛：如果实数级数 $\sum\limits_{n=1}^{\infty}u_n$ 各项的绝对值所构成的正项级数 $\sum\limits_{n=1}^{\infty}\lvert u_n \rvert$ 收敛，称级数 $\sum\limits_{n=1}^{\infty}u_n$ 绝对收敛。
- 条件收敛：如果实数级数 $\sum\limits_{n=1}^{\infty}u_n$ 收敛， 而级数 $\sum\limits_{n=1}^{\infty}\lvert u_n \rvert$ 发散，则称级数 $\sum\limits_{n=1}^{\infty}u_n$ 条件收敛。
- 定理8：如果级数 $\sum\limits_{n=1}^{\infty}u_n$ 绝对收敛，则级数 $\sum\limits_{n=1}^{\infty}u_n$ 必定收敛。 

### * 四、绝对收敛级数的性质
- 定理9：绝对收敛级数经改变项的位置后构成的级数也收敛，且与原级数有相同的和（即绝对收敛级数具有可交换性）。
- 定理10（绝对收敛级数的乘法）：设级数 $\sum\limits_{n=1}^{\infty}u_n$ 和级数 $\sum\limits_{n=1}^{\infty}u_n$ 都绝对收敛，其和分别为 $s$ 和 $\sigma$，则它们的柯西乘积

$$
    u_1v_1+(u_1v_2+u_2v_1)+\dotsb+(u_1v_n+u_2v_{n-1}+..+u_nv_1)+\dotsb
$$

也是绝对收敛的，且其和为 $s \cdot \sigma$。

## 第三节 幂级数
### 一、函数项级数的概念
- 给定一个定义在区间 $I$ 上的函数列 $u_1(x),u_2(x),u_3(x),\dotsc,u_n(x),\dotsc,$ 则由着函数列构成的表达式

$$
    \tag{1}
    u_1(x)+u_2(x)+u_3(x)+\dotsb+u_n(x)+\dotsb
$$

称为定义在区间 $I$ 上的（函数项）无穷级数或（函数项）级数。
对于每一个确定的值 $x_0 \in I$ ，函数项级数（1）成为常数项级数
    
$$
    \tag{2}
    u_1(x_0)+u_2(x_0)+u_3(x_0)+\dotsb+u_n(x_0)+\dotsb
$$

- 收敛点：若（2）在 $x_0$ 处收敛，称 $x_0$ 是函数项级数（1）的收敛点。
- 发散点同理。
- 收敛域：函数项级数（1）的收敛点的全体称为它的收敛域，发散点的全体称为它的发散域。
- 和函数：在收敛域上，函数项级数的和是 $x$ 的函数 $s(x)$ ，通常称 $s(x)$ 为函数项级数的和函数，定义域是级数的收敛域。写成

$$
    s(x)=u_1(x)+u_2(x)+u_3(x)+\dotsb+u_n(x)+\dotsb
$$

- 函数项级数（$\color{Brown}{部分和}$）：把函数项级数的前 $n$ 项的部分和记作 $s_n(x)$。
- 函数项级数（$\color{Brown}{和函数}$）：把函数项级数的前 $n$ 项的部分和记作 $s_n(x)$ ，则在收敛域上有$\lim\limits_{n\to\infty}s_n(x)=s(x)$。
- 函数项级数余项：记 $r_n(x)=s(x)-s_n(x)$，$r_n(x)$叫函数项余数的余项（在收敛域），并有$\lim\limits_{n\to\infty}r_n(x)=0$。

### 二、幂级数及其收敛性
- 幂级数：函数项级数中各项都是幂函数，它的形式是

$$
    \tag{3}
    \sum_{n=0}^{\infty}a_nx^n=a_0+a_1x+a_2x^2+\dotsb+a_nx^n+\dotsb
$$

其中，常数 $a_0,a_1,a_2,\dotsc,a_n,\dotsc$ 叫做幂级数的系数。

- 定理1（$\color{Brown}{阿贝尔（\mathrm{Abel}）定理}$）：如果级数 $\sum\limits_{n=0}^{\infty}a_nx^n$ 当 $x=x_0(x_0 \ne 0)$ 时收敛，则适合不等式 $\lvert x \rvert<\lvert x_0 \rvert$ 时的一切 $x$ 使这幂级数绝对收敛。反之，如果级数 $\sum\limits_{n=0}^{\infty}a_nx^n$ 当 $x=x_0$ 时发散，则适合不等式 $\lvert x \rvert>\lvert x_0 \rvert$ 的一切 $x$ 使这幂级数发散。
    - 推论：如果幂级数 $\sum\limits_{n=0}^{\infty}a_nx^n$ 不是仅在 $x=0$ 一点收敛，也不是在整个数轴上都收敛，则必有一个确定的正数 $R$ 存在，使得当 $\lvert x \rvert<R$ 时，幂级数绝对收敛；当 $\lvert x \rvert>R$ 时，幂级数发散；当 $x=R$ 与 $x=-R$ 时，幂级数可能收敛也可能发散。
    - 收敛半径：正数 $R$ 通常叫做幂级数（3）的收敛半径。
    - 开区间 $(-R,R)$ 叫做幂级数（3）的收敛区间。
- 定理2（幂级数的收敛半径求法）：如果 $\lim\limits_{n\to\infty}\left\lvert \dfrac{a_{n+1}}{a_n} \right\rvert=\rho$，其中 $a_n、a_{n+1}$ 是幂级数 $\sum\limits_{n=0}^{\infty}a_nx^n$ 的相邻两项的系数，则这个幂级数的收敛半径

$$
 R =
  \begin{cases}
    1/\rho    & \quad \rho \ne 0,  \\  
    +\infty   & \quad \rho = 0,  \\  
    0    & \quad \rho = +\infty. \\  
  \end{cases}
$$

### 三、幂函数的运算
设幂函数 

$$
\sum_{n=0}^{\infty}a_nx^n=a_0+a_1x+a_2x^2+\dotsb+a_nx^n+\dotsb 
$$

$$
\sum_{n=0}^{\infty}b_nx^n=b_0+b_1x+b_2x^2+\dotsb+b_nx^n+\dotsb 
$$

分别在区间 $(-R,R)$ 及 $(-R',R')$内收敛，对于这两个幂级数，可以进行加减乘除，在较小的区间内成立。

（$\color{Brown}{和函数性质}$）
- 性质1：幂级数 $\sum\limits_{n=0}^{\infty}a_nx^n$ 的和函数 $s(x)$ 在其收敛域 $I$ 上连续。
- 性质2：幂级数 $\sum\limits_{n=0}^{\infty}a_nx^n$ 的和函数 $s(x)$ 在其收敛域 $I$ 上可积，并有逐项积分公式

$$
\tag{5}
    \int_0^x s(x)\,\mathrm{d}x = \int_0^x\left[\sum_{n=0}^{\infty}a_nx^n\right]\mathrm{d}x=\sum_{n=0}^{\infty} \int_0^x a_nx^n \mathrm{d}x  \\
    =\sum_{n=0}^{\infty} \dfrac{a_n}{n+1}x^{n+1} \quad (x \in I),
$$

逐项积分后所得到的幂级数和原级数有相同的收敛半径。

- 性质3：幂级数 $\sum\limits_{n=0}^{\infty}a_nx^n$ 的和函数 $s(x)$ 在其收敛区间 $(-R,R)$ 内可导，且有逐项求导公式

$$
    \tag{6}
    s'(x)=\left(\sum_{n=0}^{\infty}a_nx^n \right)'= \sum\limits_{n=0}^{\infty}\left(a_nx^n \right)'= \sum\limits_{n=0}^{\infty}n a_nx^{n-1} \quad(\lvert x \rvert< R)
$$

逐项求导后所得到的的幂级数和原级数有相同的收敛半径。
- 反复应用上述结论，幂级数 $\sum\limits_{n=0}^{\infty}a_nx^n$ 的和函数 $s(x)$ 在其收敛区间 $(-R,R)$ 内具有任意阶导数。

## 第四节 函数展开成幂级数
### 定义
- 换句话说，也就是：能否找到这样一个幂级数，它在某区间内收敛，且其和恰好就是给定的函数 $f(x)$。如果能找到这样的幂级数，就说，函数 $f(x)$ 在该区间内能展开成幂级数。
- 假设函数 $f(x)$ 在点 $x_0$ 的某领域 $U(x_0)$ 内能展开成幂级数，即有：

$$
    \tag{1}
    f(x) =a_0+a_1(x-x_0)+a_2(x-x_0)^2+\dotsb+a_n(x-x_0)^n+\dotsb, \, x \in U(x_0)
$$

根据和函数性质，可知 $f(x)$ 在 $U(x_0)$ 内应具有任意阶导数，且

$$
    f^{(n)}(x) = n!a_n + (n+1)!a_{n+1}(x-x_0)+\dfrac{(n+2)!}{2!}(x-x_0)^2 + \dotsb,
$$

可得到 $f^{(n)}(x_0)=n!a_n$，于是 
    
$$
    \tag{2}
    a_n=\dfrac{1}{n!}f^{(n)}x_0 \quad (n=0,1,2,\dotsc)
$$

- 若函数 $f(x)$ 有幂级数展开式（1），那么该幂函数的系数 $a_n$ 由公式（2）确定，即该幂级数必为

$$
    \tag{3}
    f(x_0)+f'(x_0)(x-x_0)+ \dotsb + \dfrac{1}{n!}f^{(n)}(x_0)(x-x_0)^n + \dotsb \\
    = \sum\limits_{n=0}^{\infty} \dfrac{1}{n!}f^{(n)}(x_0)(x-x_0)^n,
$$

此幂级数（3）叫做函数 $f(x)$ 在点 $x_0$ 处的$\color{brown}{泰勒级数}$。

而展开式必为
    
$$
    \tag{4}
    f(x)= \sum\limits_{n=0}^{\infty} \dfrac{1}{n!}f^{(n)}(x_0)(x-x_0)^n, \quad x \in U(x_0)
$$

此展开式（4）为函数 $f(x)$ 在点 $x_0$ 处的$\color{brown}{泰勒展开式}$。
- 如： 函数项级数$1+x+x^2+ \dotsb + x^n + \dotsb$ 在 $\lvert x \rvert<1$ 时，这时候级数收敛于和 $\dfrac{1}{1-x}$ ;
    此时有

$$
\dfrac{1}{1-x}=1+x+x^2+ \dotsb + x^n + \dotsb \quad (-1 <x<1)
$$

- 反过来， $f(x)$可以在区间 $(-1<x<1)$ 上展开成 $1+x+x^2+ \dotsb + x^n + \dotsb$。
- 定理：设函数 $f(x)$ 在点 $x_0$ 的某一领域 $U(x_0)$ 内具有各阶导数，则 $f(x)$ 在该领域内能展开成泰勒级数的充分必要条件是在该领域内 $f(x)$ 的泰勒公式中的余项 $R_n(x)$ 当 $n \to \infty$ 时的极限为零，即：

$$
    \lim_{n \to \infty}R_n(x) = 0, \quad x \in U(x_0).
$$

- 麦克劳林级数：
- 麦克劳林展开式：
    - 第一步
    - 第二步
    - 第三步
    - 第四步

### 例题
🌰：将函数展开成x的幂级数

## 第五节 函数的幂级数展开式的应用

### 一、近似计算

### 二、微分方程的幂级数解法

### 三、欧拉公式

## * 第六节 函数项级数的一致收敛性及一致收敛级数的基本性质
### 一、函数项级数的一致收敛性
### 二、一致收敛级数的基本性质

## 第七节 傅里叶级数
### 一、三角级数 三角函数系的正交性
- 正弦函数组成的级数

$$
\tag{1}
    f(t)=A_0+\sum_{n=0}^{\infty}A_n\sin(n\omega t+\varphi_n)
$$

其中 $A_0,A_n,\varphi_n(n=,1,2,3,\dotsb)$ 是常数。

- 三角级数：令（1）中 $\dfrac{a_0}{2} = A_0, a_n=A_n\sin{\varphi _n},b_n=A_n\cos{\varphi_n},\omega = \dfrac{\pi}{l}$ （即 $T=2l$），可得：

$$
    \tag{2}
    \dfrac{a_0}{2}+\sum_{n=1}^{\infty}(a_n\cos\dfrac{n \pi t}{l}+b_n\sin\dfrac{n \pi t}{l})
$$

其中 $a_0,a_n,b_n(n=1,2,3,\dotsb)$ 是常数。令 $\dfrac{\pi t}{l}=x$，（2）变为：

$$
    \tag{3}
    \dfrac{a_0}{2}+\sum_{n=1}^{\infty}(a_n \cos nx+b_n\sin nx)
$$

周期为 $2 \pi$ 。（第一个的周期为 $2\pi$ ，第二个周期为 $\pi$，以此类推。所以三角函数周期为 $2\pi$ 没毛病。）

- 三角函数的正交性  
    - 函数正交：正交这个概念主要出现在线性代数的向量中，两个向量内积为 $0$，我们称为*向量的正交*。  
    
    那么，对于函数的正交，就可以理解两个函数内积为0，那么如何定义*函数的内积*呢？  
    首先，考虑向量 $\pmb{a}=(1,0,1)$ 和向量 $\pmb{b}=(-1,0,1)$ ，由于向量内积为 $\pmb{a}\cdot \pmb{b}= 1 \cdot -1 + 0 \cdot 0 + 1 \cdot 1 = 0$ ，所以二者正交，即*向量对应元素乘积*的和为 $0$ ，我们称为正交。同样，对于函数，我们可以把函数看成*无穷维度*的函数，比如 $f(x)=(f(1),f(2),f(3),\dotsb))$ ， $g(x)=(g(1),g(2),g(3),\dotsb))$，因此，$f(x)$ 和 $g(x)$ 的内积为 $f(x)\cdot g(x)=f(1)\cdot g(1)+f(2)\cdot g(2)+f(3)\cdot g(3)+\dotsb$ ， 学过微积分的可以发现，该式即为 $f(x)\cdot g(x)$ 在定义域上的积分。而三角函数只是特殊的正交函数罢了，类似的还有很多。。

    - 三角函数系
      
$$
    \tag{4}
    1,\cos x,\sin x,\cos 2x,\sin 2x,\dotsb,\cos nx,\sin nx,\dotsb
$$

在区间 $[-\pi,\pi]$ 上正交，指的是（4）中任何两个不同函数的乘积在区间 $[-\pi,\pi]$ 上的积分等于零。

$$
        \begin{aligned}
        & \int_{-\pi}^\pi \sin kx\, \cos nx \,\mathrm{d}x = 0\quad(k,n=1,2,3,\dotsb),\\[2ex]
        & \int_{-\pi}^\pi \sin kx\, \sin nx \,\mathrm{d}x = 0\quad(k,n=1,2,3,\dotsb,k \ne n),\\[2ex]
        & \int_{-\pi}^\pi \cos kx\, \cos nx \,\mathrm{d}x = 0\quad(k,n=1,2,3,\dotsb,k \ne n).\end{aligned}
$$

证明：积化和差求定积分。速查表：
    
$$
        \int_{-\pi}^{\pi}1^2 \mathrm{d}{x}=2\pi,\int_{-\pi}^{\pi}\sin^2 nx\,\mathrm{d}{x}=\pi,\int_{-\pi}^{\pi}\cos ^2 nx\,\mathrm{d}{x}=\pi.
$$

### 二、函数展开成傅里叶级数
设 $f(x)$ 是周期为 $2\pi$ 的周期函数，且能展开成三角级数

$$
\tag{5}
f(x)=\dfrac{a_0}{2}+\sum_{k=1}^{\infty}(a_k \cos kx+b_k \sin kx)
$$

如何利用 $f(x)$ 把 $a_0,a_1,b_1,\dotsb$ 表示出来？

- 方法：$a_0$，（5）左右积分；$a_n$，左右乘以 $\cos nx$，求积分；$b_n$，左右乘以 $\sin nx$，求积分。得
  
$$
    \left.
    \begin{aligned}
    &a_n=\dfrac{1}{\pi}\int_{-\pi}^{\pi}f(x)\cos nx \,\mathrm{d}{x}\quad(n=0,1,2,3,\dotsb),\\
    &b_n=\dfrac{1}{\pi}\int_{-\pi}^{\pi}f(x)\sin nx \,\mathrm{d}{x}\quad(n=1,2,3,\dotsb).\end{aligned}
    \right\}\tag{6}
$$

- 傅里叶系数： $a_n,b_n$ 叫做函数 $f(x)$ 的傅里叶系数。
- 傅里叶级数：将傅里叶系数（6）带入（5）中得到的三角级数叫做函数 $f(x)$ 的傅里叶级数。 
- 收敛定理（狄利克雷（Dirichlet）充分条件）：设 $f(x)$ 是周期为 $2\pi$ 的周期函数，如果它满足：
    - （1）在一个周期内连续或只有有限个第一类间断点，
    - （2）在一个周期内之多只有有限个极值点，  

则 $f(x)$ 的傅里叶级数收敛，并且  
当 $x$ 是 $f(x)$ 的连续点，级数收敛于 $f(x)$；  
当 $x$ 是 $f(x)$ 的间断点，级数收敛于 $\dfrac{1}{2}[f(x^-)+f(x^+)]$。 

- PS：物理世界中函数 $f(x)$ 的傅里叶级数都收敛。



### 三、正弦级数和余弦级数
### 🌰

## 第八节 一般周期函数的傅里叶级数
### 一、周期为 $2l$ 的周期函数的傅里叶级数
- 定理： 设周期为 $2l$ 的周期函数 $f(x)$ 满足收敛定理的条件，则它的傅里叶级数展开式为
  
$$
\tag{1}
    f(x) = \dfrac{a_0}{2}+ \sum_{n=1}^{\infty} \left(a_n \cos \dfrac{n\pi x}{l} + b_n \sin  \dfrac{n\pi x}{l} \right)\,(x \in C),
$$

其中，

$$
\left.
    \begin{aligned}
    & a_n = \dfrac{1}{l} \int_{-l}^{l}f(x) \cos \dfrac{n\pi x}{l} \mathrm{d}{x}\,(n=0,1,2,\dotsb),\\[2ex]
    & b_n = \dfrac{1}{l} \int_{-l}^{l}f(x) \sin \dfrac{n\pi x}{l} \mathrm{d}{x}\,(n=1,2,\dotsb).\\[2ex]
    \end{aligned}
    \right\}    \tag{2}
$$

$$
C=\{x| f(x)= \dfrac{1}{2}[f(x^-)+f(x^+)] \}
$$

证明，令 $z=\dfrac{\pi x}{l}$，区间 $-l \le x \le l$ 就变换成 $-\pi \le z \le \pi$。

### 二、傅里叶级数的复数形式
将（1）、（2）利用欧拉公式

$$
\cos t= \dfrac{\mathrm{e}^{\mathrm{i}t}+\mathrm{e}^{\mathrm{-i}t}}{2},\quad \sin t= \dfrac{\mathrm{e}^{\mathrm{i}t}-\mathrm{e}^{\mathrm{-i}t}}{2\mathrm{i}}
$$

得傅里叶级数的复数形式为

$$
\tag{11}
\sum_{n = -\infty}^{\infty} c_n \mathrm{e} ^ {\mathrm{i} \tiny{\dfrac{n\pi x}{l}}}
$$

其中

$$
\tag{12}
c_n =\dfrac{1}{2l} \int_{-l}^{l}f(x) \mathrm{e} ^ {\mathrm{-i }\tiny{\dfrac{n\pi x}{l}}} \mathrm{d}{x}\quad (n=0, \pm1, \pm2, \dotsb).
$$

### 🌰

## Reference
[1*] 同济大学数学系, 高等数学（上册）. 高等教育出版社, 2007.

