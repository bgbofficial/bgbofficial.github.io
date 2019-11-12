---
layout: post
title: 数字图像分析@02 *Signal-1D Fourier Alysis*
date: 2019-11-01 
tag: Signal
mathjax: true
---

# Chapter-3 Fourier Transform

## 3.2 周期信号的傅里叶级数分析

### （一）三角函数形式的傅里叶级数

$\qquad$由数学分析课程已知，周期函数 $f(t)$ 可由三角函数的线性组合来表示，若 $f(t)$ 的周期为 $T_1$，角频率为 $\omega=\dfrac{2\pi}{T_1}$，频率$f_1=\dfrac{1}{T_1}$，傅里叶级数展开表达式为

$$
\begin{aligned}
f(t) 
&=a_0 +a_1\cos{(\omega_1t})+b_1\sin{(\omega_1t})+a_2\cos{(\omega_2t}) +\\[2ex]
& \quad b_2\sin{(\omega_2t})+ \dotsb + a_n\cos{(\omega_1t})+b_n\sin{(\omega_1t})+\dotsb\\
&=a_0+\sum_{n=1}^{\infty}[a_n\cos{(n\omega_1t)+b_n\sin{(n\omega_1t})}]
\end{aligned}\tag{3-1}
$$

其中 $n$ 为正整数，各个谐波成分的幅度值按下各式计算：  
$\qquad$直流分量
$$
a_0 = \dfrac{1}{T_1}\int_{t_0}^{t_0+T_1}f(t) \mathrm{d}{t}\tag{3-2}
$$

$\qquad$余弦分量的幅度

$$
a_n = \dfrac{2}{T_1}\int_{t_0}^{t_0+T_1}f(t)  \cos{(n \omega_1 t)}\, \mathrm{d}{t}\tag{3-3}
$$

$\qquad$正弦分量的幅度

$$
b_n = \dfrac{2}{T_1}\int_{t_0}^{t_0+T_1}f(t)  \sin{(n \omega_1 t)}\, \mathrm{d}{t}\tag{3-4}
$$

其中 $n=1,2,\dotsb$。

将式（3-1）中同频率项加以合并，可以写成另一种形式

$$
f(t) = c_0 +\sum_{n=1}^{\infty} c_n\cos{(n\omega_1t+ \varphi_n)}\tag{3-5}
$$
或

$$
f(t) = d_0 +\sum_{n=1}^{\infty} d_n\sin{(n\omega_1t + \theta_n)}
$$
比较（3-1）和（3-5）得出变量关系

$$
\left.\begin{aligned}
& a_0 = c_0 = d_0 \\[2ex]
& c_n = d_n =  \sqrt{a_n^2 + b_n^2} \\[2ex]
& a_n = c_n \cos\varphi_n = d_n \sin\theta_n \\[2ex]
& b_n = -c_n\sin \varphi_n = d_n\cos \theta_n \\[2ex]
& \tan \theta_n = \dfrac{a_n}{b_n} \\[2ex]
& \tan \theta_n = - \dfrac{b_n}{a_n} \\[2ex]
& (n=1,2,\dotsb)
\end{aligned}\right\}\tag{3-6}
$$

$\qquad$各个正、余弦分量的频率 $(n=1,2,\dotsb)$ 必定是基频 $f_1(f_1=1/T_1)$ 的整数倍 $(f_1,2f_1,3f_1,\dotsb)$。  
$\qquad$从式子（3-3）到（3-6）看出，各个分量幅值 $a_n,b_n,c_n$ 及相位 $\varphi_n$ 都是 $n\omega_1$ 的函数。可以把 $c_n-n\omega_1$ 和 各分量的相位 $\varphi_n-n\omega_1$ 关系图画出，分别得到幅度频谱和相位频谱。  

![3-1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191108092825.png)  
$\qquad$周期信号频谱只会出现在 $0,\omega_1,\omega_2,\dotsb$ 离散谱上。

### （二）指数形式的傅里叶级数
$\qquad$将周期信号的傅里叶级数表示成指数形式，已知

$$
f(t)=a_0+\sum_{n=1}^{\infty}[a_n\cos{(n\omega_1t)+b_n\sin{(n\omega_1t})}]\tag{3-7} 
$$
根据欧拉公式 $^{[5]}$

$$
\begin{aligned} &\cos{(n\omega_1t)}=\dfrac{1}{2}(e^{\mathrm{j}{nw_1t}}+e^{\mathrm{-j}{nw_1t}})\\[2ex] & \sin{(n\omega_1t)}=\dfrac{1}{2\mathrm{j}}(e^{\mathrm{j}{nw_1t}}-e^{\mathrm{-j}{nw_1t}})\end{aligned}
$$

把欧拉公式带入（3-7）得到

$$
f(t)=a_0 + \sum_{n=1}^{\infty}\left(\dfrac{a_n-\mathrm{j}b_n}{2}\mathrm{e}^{\mathrm{j}n\omega_1t} + \dfrac{a_n +\mathrm{j}b_n}{2} \mathrm{e}^{-\mathrm{j}n\omega_1t}  \right)\tag{3-8}
$$
令

$$
F(n\omega_1)=\dfrac{1}{2}(a_n-\mathrm{j}b_n) \qquad(n=1,2,\dotsb)\tag{3-9}
$$

$\qquad$由于 $a_n$ 是 $n$ 的偶函数， $b_n$ 是 $n$ 的奇函数[见（3-3）/（3-4）]，由式子（3-9）推出

$$
F(-n\omega_1)=\dfrac{1}{2}(a_n+\mathrm{j}b_n) \qquad(n=1,2,\dotsb)
$$

上述两个式子带入（3-8）得到

$$
f(t)=a_0+\sum_{n=1}^{\infty} [F(n\omega_1)\mathrm{e}^{\mathrm{j}n\omega_1t}+F(-n\omega_1)\mathrm{e}^{\mathrm{-j}n\omega_1t}]
$$
令 $F(0)=a_0$，并且

$$
\sum\limits_{n=1}^{\infty}F(-n\omega_1)\mathrm{e}^{\mathrm{-j}n\omega_1t}=\sum\limits_{n=-1}^{-\infty}F(n\omega_1)\mathrm{e}^{\mathrm{j}n\omega_1t}
$$

得到 $f(t)$ 的指数形式傅里叶级数，为

$$
f(t)=\sum_{n=-\infty}^{\infty}F(n\omega_1)\mathrm{e}^{\mathrm{j}n\omega_1t}\tag{3-10}
$$
$\qquad$将（3-3）、（3-4）带入（3-9）得到指数形式傅里叶级数系数 $F(n\omega_1)$ 或简写为 $F_n$，等于

$$
F_n=\dfrac{1}{T_1}\int_{t_0}^{t_0+T_1} f(t)\mathrm{e}^{-\mathrm{j}n\omega_1t}\, \mathrm{d}{x}
\tag{3-11}
$$
其中 $n \in (-\infty,+\infty)$ 的整数。
$\qquad$从式（3-6）、（3-9）中看出， $F_n$ 与其他系数有如下关系


$$
\left.\begin{aligned}
& F_0 = c_0 = d_0 = a_0 \\[2ex]
& F_n = \vert F_n \rvert \mathrm{e}^{\mathrm{j}\varphi_n}=\dfrac{1}{2}(a_n-b_n) \\[2ex]
& F_{-n} = \vert F_{-n} \rvert \mathrm{e}^{\mathrm{-j}\varphi_n}= \dfrac{1}{2}(a_n+b_n) \\[2ex]
& \vert F_n \rvert = \vert F_{-n} \rvert = \dfrac{1}{2}c_n = \dfrac{1}{2}d_n = \dfrac{1}{2}\sqrt{a_n^2 + b_n^2} \\[2ex]
& \vert F_n \rvert + \vert F_{-n} \rvert =c_n \\[2ex]
& F_n + F_{-n} = a_n \\[2ex]
& b_n = \mathrm{j}(F_n - F_{-n}) \\[2ex]
& c_n^2 = d_n^2 = a_n^2 + b_n^2 = 4F_nF_{-n} \\
& \qquad (n=1,2,1\dotsb) 
\end{aligned} \right\} \tag{3-12}
$$
由于 $F_n = |F_n|\mathrm{e}^{\mathrm{j}\varphi_n}$，可以画出复数幅度谱 $|F_n|-\omega$ 与复数相位谱 $\varphi-\omega$，且 $|F_n| = \dfrac{1}{2}c_n$。

周期信号 $f(t)$ 的平均功率 $P$ 与傅里叶系数由下列关系

$$
\begin{aligned}P
& = \overline{f^2(t)}= \dfrac{1}{T_1}\int_{t_0}^{t_o+T_1}f^2(t)\, \mathrm{d}t \\[2ex]
& = a_0^2 + \frac{1}{2}\sum_{n=1}^{\infty}(a_n^2 + b_n^2)=c_0^2+ \frac{1}{2}\sum_{n=1}^{\infty}c_n^2 \\[2ex]
& =\sum_{n=-\infty}^{\infty}|F_n|^2
\end{aligned}\tag{3-13}
$$

表明：时域和频域能量守恒，称为帕赛瓦尔定理。

### （三）函数的对称性和傅里叶系数的关系


## 💥积分变换的解释

### 积分变换的投影解释 $^{[3]}$

函数在不同基的空间中的投影。  
解释详细点吧首先这些变换都是数学概念，不要想得很具体，不然很容易头晕  
积分实际上就是内积运算，而我们知道，向量a与方向向量i的内积，就是a在i方向上的投影。如果向量a和不同方向的向量分别求内积，得到的就是在各个方向上的分量。  
如果方向向量满足正交，完备， 则这组向量是一组基。 

举个例子，三维空间中，(0,0,1); (0,1,0); (1,0,0)就是一组基，而这个空间中任何一个向量都可以被这三个向量的线性表示。  
被投影到基向量上以后，向量的运算变得更方便。比如知道两个向量的长度和方向，转换成（x，y，z）形式会更容易运算点乘和差乘。  
之前所说可以总结为，"向量投影到基上，便于运算"。   
接下来把这个推广到函数上。  
不论是傅里叶，拉普拉斯，还是z， 都在做积分运算，而且都是和某一类函数做积分。  
积分就是内积，就是投影。换句话说，原函数被分解为一系列函数的线性叠加。  
那么这一系列函数，其实就是基向量（在此不做证明），区别于三围空间的是，这一组基有无穷多个。  

Fourier 是分解到正弦函数  
Laplace 是分解到幅度指数变化的正弦函数  
Z是分解到周期变化的离散序列  

对于复数的情况，其实是一样的，只是基的选择改变了。变换的好处就是，便于运算。这一点也不赘述，有体验的人都能感受到所以，最形象的解释就是，这三种变换，都是向量的投影运算，通过不同方向投影的分析，来分析没有投影前的向量。我的建议是，以后看待他们，就像看待向量的分解一样，会少很多纠结。    

有人提到了解方程或者换一个域便于解答，其实都比较表象，只是应用之一。而且这三种变换本身也只是积分变换的一个部分。从国内本科的分科方式来看，这些东西看起来是微积分，但是内核还是更接近于线性代数。其实从拓扑空间开始考虑，貌似这两门课的区别本质上并不是很大，原理是一样的，或者至少很像。

### 积分变换是波粒二象性在数学中的体现 $^{[4]}$

微观粒子的波动性是绝对不可以忽略的。这也是量子力学和固体物理里许多非常著名的结论和定理的基础。比如固体物理学里研究一个非常著名的问题就是固态晶体材料的热传导特性。起初人们用统计物理的手法做了一个非常漂亮，也非常简单的模型。只是后来人们发现这个模型怎么都描述不对真实的过程，和实验的吻合实在太差。后来发现原来是粒子的波动性不可忽视所导致的（这一个问题也成了量子力学理论正确性的一个著名佐证）。因此我们发现要把微观系统的这一套模型写好，是必须考虑波动性质的。（将粒子态到波态转化的过程，所需要的数学方法就是傅里叶变换。与此同时，其逆过程，正是逆傅里叶变换。）  

傅里叶变换一方面是一个数学工具，而另一方面，从某种意义上讲，他正是波粒二相性的数学表达（波态是物质波或者粒子波，粒态是宏观物体或者微观物质）。  

这个里头，熟悉固体物理的朋友其实恐怕已经意识到了。就是在晶体学和固态材料的研究中我们经常会用到的那个“k空间（波矢空间）。”其实比如一个钙钛矿晶体（用晶体点阵模型表示）和这个晶体的k空间状态，说白了其实都是一个“存在”的两个“像”而已。这好比我们眼睛所见到的事物，与事物的影子。

### 为什么坐标空间的傅立叶变换是动量空间？如何理解？ $^{[6]}$
如果看傅里叶变换的核，可以发现都是的形式，其中是的共轭量，因为傅里叶变换本来就是受启发于傅里叶级数，而傅里叶级数就是一个以三角函数为基矢的级数。所以逻辑上严格地讲，并非量子态展开到一组基矢上，这组基矢恰好是傅里叶变换的核（私以为所有“恰好”，“刚好”都应该谨慎使用）。而是，我们要进行傅里叶变换，自然要用到傅里叶变换的核，而我们知道傅里叶变换的核都是的形式。注意到，指数函数上面的指数应该是无量纲的数，所以，如果一个中的是时间，对应的量纲就是，也就是频率的量纲，对所有积分之后得到的是一个的函数。所以我们说一个时域的函数傅里叶变换之后就变成频域的函数。而如果中的是坐标，那么就应该是的量纲，也就是与波数的量纲相同。而（这里的是动量，哎我的notation果然一直都很糟糕）。是一个（有量纲的）常数。对所有积分之后得到一个或者（动量）的函数。这样，我们就可以说，坐标空间傅里叶变换之后是动量空间。

### 动量空间-波矢空间-k空间 $^{[7]}$
在三维实空间里，一个点粒子系统的每个粒子的有坐标(x, y, z)，或者把这个坐标，看成是向量的三个分量，写成向量r。然而，这对于描述运动的粒子是不够的——除了位置，我们还想要知道粒子的速度，或者说动量 p。对一个N粒子系统，它的坐标为(r1,r2,..rN)，表示粒子1处在坐标r1上，粒子2处在r2上，... ，粒子N处在坐标rN上；而动量的**为(p1,p2, .., pN)，即第k个粒子的动量为pk。

就这样，我们得到了一个新的空间。在这个新空间里，我们并不关心粒子的坐标是多少，只关心它具有多少动量。这就是动量空间。

为什么需要这个空间呢？考虑如下场景。现在我们有一升的理想气体，盛在封闭容器里，里面大约有10^22个气体原子。我们不写出每个原子的位置，只知道它们在容器里均匀分布，也就是有一恒定密度[在这里我们不考虑热力学涨落的问题]。

真正有趣的事情发生在动量空间。虽然在实空间里粒子密度均匀，但并非所有粒子都具有一样的速率。我们做不到跟踪每个粒子速率，但是我们可以写出它们的速率
的分布。类比在实空间里的密度概念，我们可以把这个分布理解为速率的密度。速率密度大的地方，就表示处于这段速率的粒子数目多。

# Reference

[1*] 郑君里, 应启珩, and 杨为理, 信号与系统. 高等教育出版社, 2000. 

[2] 谷超豪等, 数学物理方程. 高等教育出版社, 2002.  

[3] [怎么通俗地介绍拉普拉斯变换、傅里叶变换和 z 变换？](https://www.zhihu.com/question/19983179/answer/26686107)  

[4] [Quantum Mechanics and the Fourier Transform](https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Supplemental_Modules_(Physical_and_Theoretical_Chemistry)/Quantum_Tutorials_(Rioux)/Quantum_Fundamentals/04.1%3A_Quantum_Mechanics_and_the_Fourier_Transform)  

[5] [欧拉公式的意义](https://www.zhihu.com/question/23074201/answer/23524103)  

[6] [为什么坐标空间的傅立叶变换是动量空间？如何理解？](https://www.zhihu.com/question/22396883?sort=created)  

[7] [动量空间: 物理的状态,就活在那些基础状态组成的态空间](http://blog.sina.com.cn/s/blog_727942e70102wmmh.html)