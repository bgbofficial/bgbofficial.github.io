---
layout: post
title: Iteration Reconstruct(CH6) in MRI-03
date: 2019-11-11
tag: MRI
mathjax: true
---

#  § Iteration Reconstruct(CH6) 1st

## Outline

计算机断层成像（Computed Tomography）技术，是利用 $X$ 射线（波长极短，能量很大的电磁波，医学上应用的X射线波长约在0.001～0.1 纳米之间）、$\gamma$ 射线或可见光等作为成像介质，光源和探测器围绕目标沿着一定轨道做多角度扫描，获得射线投影，经过计算机计算，可得到物体内部图像。其他医学成像技术还包括超声成像（Ultrasonography，US），磁共振成像（Magnetic Resonance Imaging，MRI），PET，SPECT，FMT，BLT，CLT，OCT等。

通常，获取高分辨率结构图像可以使用X-CT，获取良好的软组织图像可以使用MRI。下面来计算射线投影数据到图像的过程。传统方法包括：

解析方法（二维FBP，三维FDP）和迭代重建（ART等）；

新兴方法包括：压缩感知$^{3}$重建（迭代重建，包括凸优化算法、贪婪迭代算法、最小全变分法），压缩感知低秩模型，压缩感知深度网络模型（SDA、ReconNet、ADMM_Net：DR2-Net）；深度学习重建$^5$：RED-CNN、 LEARN。

加速：CUDA并行。

本章是`迭代重建`。

1. 解线性方程组
2. 代数重建算法（Algebraic Reconstruction Technique，ART）
3. 梯度下降法
4. ML-EM（利用求最大期望值来求最大似然函数）
5. OS-EM（分成有序的子集来求期望值的极大值）
6. 噪声控制
   - 解析方法-加窗函数
   - 迭代方法-提前停止迭代
   - 迭代方法-选择像素模型
   - 迭代方法-精确建模
7. 噪声
8. 利用先验知识（贝叶斯法则）


## 1. 解线性方程组

之前的FBP等算法是指解析算法。使用体素（volumetric pixel，voxel）来代替像素的概念，不管是在二维还是三维中。代数迭代以ART为代表，另外还有MART、SART、MLEM、OSEM等。它们有共同的计算步骤：（1）投影运算，即计算当前结果的投影值；（2）计算偏差，即计算重建图像的投影值和实际测量值之间的偏差；（3）反投影计算，即把偏差映射到图像空间；（4）更新图像，修正当前估计的图像。











# Reference 

[1*] G. L. Zeng, Medical Image Reconstruction. Berlin, Heidelberg: Springer Berlin Heidelberg, 2010.

[2*] 窦少彬. CT图像优化重建算法研究[D].中国科学技术大学,2019.

[3] [压缩感知算法总结]( https://blog.csdn.net/weixin_41311617/article/details/89460443 )

[4] code：[CSDN压缩感知matlab代码]( https://blog.csdn.net/Di_Wong/article/details/81191211 )--[CS原理]( https://blog.csdn.net/Di_Wong/article/details/81191211 )--[github:CS-MoCo-Lab]( https://github.com/thomaskuestner/CS_MoCo_LAB )

[5] [腾讯：深度学习重建]( https://cloud.tencent.com/developer/news/311587 )



