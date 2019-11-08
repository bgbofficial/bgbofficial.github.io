---
layout: post
title: 数字图像分析-06 *卷积感性理解*
date: 2019-11-08 
tag: math, signal
mathjax: true
---


#  § Understanding Convolution

## 1. 一维卷积

### 1.1 离散卷积和

$$
y[n]=\sum_{k=-\infty}^{\infty}x[k]h[n-k]\tag{1}
$$

这就是离散的卷积和公式。其中$h[k]$ 是系统响应，$h[n-k]$ 是平移后的系统响应，$x[k]$ 是外界输入。$y[n]$ 是系统在 $n,(n\in[-\infty],+\infty)$ 时刻 ，系统 $h[k]$ 在 $x[k]$ 的响应。

### 1.2 物理学解释

玩游戏时，使用我方英雄`诺克萨斯之手`的w技能对对方影响造成了一次攻击。攻击的效果假设是在接下来的5秒内，敌方英雄会持续增长流血，每秒掉 $1,2,3,4,5$。现在，在第 $0$ 秒内用w技能对敌方造成了攻击，敌方流血情况为：

![01](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191108030423.png)

抽象一下，假设 $x[k]$ 是一个单位信号（一次攻击），即当且仅当 $k=0$ 时 $x(k)=1$。假设把这个信号输入到一个系统里面得到的响应为里面的响应为 $h[n]$：

![02](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191108033820.png)

同样的，假如在第 $2$ 秒对敌方攻击了，那么敌方英雄会在 $2-7$ 秒内持续掉血。

由于攻击不是在第 $0$ 秒，而是在第 $2$ 秒，因此，产生伤害也是从第 $2$ 秒产生。可以使用位移函数，则本来在第 $0$ 秒产生的伤害右移两个单位，成为函数 $h[n-2]$。

![03](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191108034527.png)

多次攻击：如果第 $0$ 秒和第 $2$ 秒都进行了攻击，伤害将是第 $0$ 秒和第 $2$ 秒伤害的叠加。如：

![04](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191108034750.png)

那么，如果`诺克萨斯之手`对敌方英雄在时间 $[t_0,t_1]$ 内，多次的攻击 $x[k],k\in[t_0,t_1]$，可以推广，计算伤害：

$$
y[n]=\sum_{k=t_0}^{+\infty}x[k]h[n-k]
$$

这就是卷积公式（离散卷积和）。解释就是，如敌方英雄仅受到诺克萨斯之手在时间 $[t_0,t_1]$ 内的攻击，那么受到的伤害（可以看做成一个LTI系统）可以从 $t_0$ 开始算起；若诺克萨斯之手的伤害会让敌方一直流血，那么时间上可以计算到 $+\infty$。

所以，如果诺克萨斯之手进行了多次攻击，敌方某一秒受到的伤害可以这样计算（也就是，对于输入 $x[k]$ ，任意一个 $y[n]$ 的伤害数值是怎么样的呢）：

![05](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191108040241.png)

如图， $k$ 代表时间，把不同关于 $n$ 的函数 $h[n-k]$ 全部画出来，如上图。那么第 $3$ 秒敌方英雄受到的伤害 $y[3]$ 为：

$$
y[3]= x[0]h[n]+x[1]h[n-1]+x[2]h[n-2]+x[3]h[n-3]
$$

### 1.3 数学解释

离散信号下，卷积 $y[n]=x[n] \ast h[n]$ ，可以理解为：将 $y[n]$ 分为不同的分量为 $h[n-k]$、系数为 $x[k]$的线性组合。也就是说，$y[n]$ 是：一系列关于 $h[n]$ 移位后的 $h[n-k]$，每个 $h[n-k]$ 的系数是 $x[k]$ 的函数。

用不同的函数的线性组合，表示原信号；

傅里叶分析用的是不同正弦函数的线性组合；

卷积用的是 $h[n]$ 移位不同的 $k$ 后，得到一系列 $h[n-k]$ 的线性组合。

### 1.4 卷积中的滤波

式子 $y[n]=x[n]\ast g[n]$ 中系统响应函数 $g[n]$ 与滤波器的区别。

问：为什么对图像边缘？这里讨论一维滤波情况。二维滤波在下面讨论。

卷积等价于在用傅里叶变换之后频域做乘法。

时域卷积就是频域相乘，其实也是在滤波。不同的地方是卷积核不同，导致频率分量不同，是高频分量通过还是低频分量通过。不少卷积算法就是用FFT实现的。



### 1.5 神经网络的一维卷积

此处可能参考了参考文献$^{4}$。

![06](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191108055050.png)

设 $f[n]=[1,1,2,-1,1,-2,1]$，则分别计算两种情况下的结果：

（1）在神经网络计算中设计一个卷积核 $\boldsymbol{G}=[1,0,-1]$：

上图可以看到NN卷积运算结果，为 

$$
\boldsymbol{Y}=[y[3],y[4],y[5],y[6],y[7]]=[-1,2,1,1,0]
$$

可以看出，$\boldsymbol{Y}$ 若不补零，则是从 $y[3]$ 开始，$y[7]$ 结束。表示每个卷积核都参与了。补零的话，会有卷积核不参与其中的运算。

（2）在信号处理计算中设计一个系统响应函数 $g[n]=[-1,0,1]$ or滤波器？：

首先计算 $y'[2],where,y'[2]=y[3]$，注意角标的不同，则 

$$
\begin{aligned}
y'[2]
& =\sum_{k=0}^{2}f[n]g[n-k] \\[2ex]
& =f[0]g[2]+f[1]g[1]+f[2]g[0] \\[2ex]
& = \begin{bmatrix}1&1&2\end{bmatrix}\cdot
\begin{bmatrix}-1\\0\\1\end{bmatrix} \\
& = -1
\end{aligned}
$$

可以看出，我们是从 $y'[2],where,y'[2]=y[3]$ 直接开始算的。并且， $g[n]=[-1,0,1]$ 是 $\boldsymbol{G}=[1,0,-1]$ 的翻转（flip）。

结论：其实，计算是差不多的，但是信号处理是将另一函数进行了翻转，而CNN并没有翻转。因为在CNN中，翻转与不翻转的问题并没有实际意义，权重更新对于翻转没有意义。忽略翻转的话就是同一个东西。神经网络里实际实现其实是算相关，后面一项是 $g(t-n)$。 考虑到神经网络中卷积核的参数是通过学习得来的，而且带有旋转不变形，卷积核的参数旋转或不旋转对结果影响不大 。

## 2. 二维卷积运算

其目的是比较信号处理中的`卷积`和神经网络中的`卷积`异同 $^{[2]}$。实际都是互相关运算。将在将来讲解。信号与系统里面的卷积可以认为是一个信号对另外一个信号进行时间维度上的扫描，得到的结果就是两个信号在时间维度上的相关度；而卷积神经网络里面的卷积是一个信号对另外一个信号进行空间维度上的扫描，得到的是平面上两个信号在空间维度上的相关度。 

### 2.1 平滑处理

对图像进行信号卷积运算：

对图像进行神经网络卷积运算：



### 2.2 卷积与傅里叶变化滤波比较

这里参考文献$^{3}$做了很好的说明。下面进行验算。



## 3. 相关运算

卷积与相关运算的关系$^{5}$。

（1）卷积。上面讨论了卷积，下面写出来，同时给出连续和离散形式：

$$
\begin{aligned}& f(t)\ast g(t)=\int_{-\infty}^{+\infty}f(\tau)g(t-\tau)\mathrm{d}{\tau}
=\int_{-\infty}^{+\infty}f(t-\tau)g(\tau)\mathrm{d}{\tau}
=\int_{-\infty}^{+\infty}f(\tau)g(-(t-\tau))\mathrm{d}{\tau} \\[2ex]
& f[n] \ast g[n] = \sum_{k=-\infty}^{+\infty}f[k]g[n-k]
\end{aligned}
$$

（2）互相关，注意这里变换过后，卷积里是 $t$，互相关里是 $\tau$， 卷积比自相关多了一步“卷”的操作 ，$t\to\tau$：

$$
\begin{aligned}& f(\tau)\ast g(\tau)=\int_{-\infty}^{+\infty}f(t)g(t+\tau)\mathrm{d}{t}
=\int_{-\infty}^{+\infty}f(t-\tau)g(\tau)\mathrm{d}{t}
=\int_{-\infty}^{+\infty}f(\tau)g(-(t-\tau))\mathrm{d}{t} \\[2ex]
& f[n] \ast g[n] = \sum_{k=-\infty}^{+\infty}f[k]g[n+k]
\end{aligned}
$$

（3）自相关：

$$
\begin{aligned}& f(t)\ast f(t)=\int_{-\infty}^{+\infty}f(\tau)f(t-\tau)\mathrm{d}{\tau}
=\int_{-\infty}^{+\infty}f(t-\tau)f(\tau)\mathrm{d}{\tau}
=\int_{-\infty}^{+\infty}f(\tau)f(-(t-\tau))\mathrm{d}{\tau} \\[2ex]
& f[n] \ast f[n] = \sum_{k=-\infty}^{+\infty}f[k]f[n-k]
\end{aligned}
$$

下面是维基的图比较：

![07](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191108092312.png)

可以看到有不同。


## 4. 图像压缩，将空域转换到频域

自然图像经过FT变换之后，图像的信息主要集中在了低频部分$^{5}$。而高频部分的系数很小，几乎可以忽略。直接将高频部分置为0，保留低频分量，就得到了图像在频域的稀疏表示。稀疏域不仅包括频域，还包括了小波域，PCA域等等。得到信号最稀疏的表示可以参考压缩感知理论。压缩感知（或稀疏编码）在图像的压缩、重建、去燥、超分辨率等中得到了很多应用。

# Reference

[1] [解释卷积]( https://www.zhihu.com/question/22298352/answer/637156871 )

[2] [信号卷积到神经网络卷积]( https://www.zhihu.com/question/22298352 )

[3] [对图像边缘处理卷积与傅里叶]( https://www.zhihu.com/question/300468921 )

[4] [信号滤波与NN卷积]( https://zhuanlan.zhihu.com/p/28478034 )

[5] [图像压缩]( https://www.zhihu.com/question/39689253 )

[6] [卷积、互相关、自相关]( https://zhuanlan.zhihu.com/p/62292503 )

