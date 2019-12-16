## 0. 数据

### 0.1 数据简介

**来源**：由纽约大学朗格医学中心提供的匿名数据集，包括了几个子数据集，它们都是原始k空间数据。为了匿名，原始数据格式转换为[ISMRMD](http://ismrmrd.github.io/)（与供应商无关的格式，并且抹除病人信息），DICOM文件也使用RSNA的工具进行了匿名化。

**膝关节MRI**：包括1500例在 3T和1.5T 下全采样的膝关节MRI；一万个3或1.5T下的临床膝关节DICOM图像。原始数据集包括有和没有脂肪抑制的冠状质子密度加权图像。DICOM数据集包含有和没有脂肪抑制的冠状面质子密度、有脂肪抑制的轴向质子密度、矢状面质子密度和有脂肪抑制的矢状面T2密度。

**脑部MRI**：包括在3T和1.5T下获得的7002份完整采样的脑部MRI数据。原始数据集包括轴向T1加权，T2加权和FLAIR图像。 一些T1加权的采集中加入了造影剂。对比和场强的确切分布在表1中给出。

![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191204032149.png)

使用：[数据](https://fastmri.med.nyu.edu/)下载在线申请，且数据的使用要遵循协议。

### 0.2 数据详情

**原始多线圈k空间数据**：未处理的原始复数多线圈核磁采集，原始MRI数据包括1,594个膝关节volumes，包括了56,987个slices（每个slice对应一个图片）；

**模拟单线圈k空间数据**：用模拟的方法将多线圈采集数据转换成单线圈采集数据[^1]；

**Ground-truth 图像集**：从多线圈全采样中重建的图像。作为挑战赛的量化参考答案，不会放到网上；

**DICOM 图像集**：在获取过程中丢弃原始数据的空间分辨率图像，可以作为额外的训练数据。这些数据来自不同的采集方法，不同的设备，不同的诊所，不同的重建方法，不同的后处理算法。将这些数据应用迁移学习的思想来作为挑战算法的一部分可能效果会很好。官方还将放出这些膝关节DICOM数据，来自于不同医院的10,000膝盖检查，包含了超过1.2百万个slices。

总的来说，每个原始volume被随机放入：训练集、验证集、多线圈测试集、单线圈测试集、多线圈挑战集和单线圈挑战集。下表Table3展示了Volumes的分配情况。测试集未放出，是上传查看结果。挑战集在将来会放出。

![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191204041916.png)

**任务1**：从欠采样的单线圈中重建图像，尽量接近Ground-truth。

**任务2**：从欠采样的多线圈中重建图像，尽量接近Ground-truth。

每个任务官方提供了已经做好的 *训练集* 和 *验证集* ，包含了全采样的k空间数据和全采样ground-truth；*测试集* 和 *挑战赛数据*  包含了使用笛卡尔欠采样掩码后的全采样k空间数据。

**笛卡尔欠采样MASK**：

- 为了加速2D-MRI成像，k空间掩码线主要是在相位编码上；

- 每个Volume的所有slices都用同一个mask；
- 为了采集多样性，每个mask都是随机选择的。首先，4x或者8x的加速因子随机选择；然后，下采样掩码首先要包含若干相邻的最低频率k空间线，以此来提供一个完全采样的k空间区域。当加速因子是4，全采样的中心区域包含了全部k空间线的8%；当为8时，则相应的为4%；剩余的k空间线，通过预设的概率，一致地被随机包含选择。平均来说，欠采样掩码实现了理想的加速效果。
- 随机欠采样是为了通用情况下的压缩感知[^2] [^3]。

![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191204042634.png)

## 1. fastMRI挑战 2019.09.05--2019.09.19

说明：这里是官方的网站 https://fastmri.org/ ，和详细说明 [PDF:arxiv fastMRI](https://arxiv.org/pdf/1811.08839.pdf )。官方文档对MRI做了基本的介绍，并且介绍了基础的深度学习重建算法和Baselines。

数据：2019.09.05放出挑战 [数据集](https://fastmri.med.nyu.edu/)，并且可以开始提交结果，挑战只能使用官方数据集（膝盖MRI），[Challenge leaderboard](https://fastmri.org/leaderboards/challenge) 提交截止日在2019.09.19；[Public Leaderboard](https://fastmri.org/leaderboards) 应该可以一直提交，目前没有看见对于截止日的说明。

形式：单线圈（4倍加速），多线圈（4倍和8倍加速），一共三组。结果在Challenge leaderboard上。

提交：根据 [提交指南](https://fastmri.org/submission_guidelines)，进行提交。包括：1页关于算法的报告（可以被公开看见，如下图），和使用在 [github](https://github.com/facebookresearch/fastMRI) 上的官方工具提交训练模型等等。

![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191204022322.png)

排名：比赛首先按照SSIM来排序，并且会被来自不同机构的人员组成的放射学专家组审核，专家组会通过SSIM和视觉质量决定谁是winner。

## 2. 结果：
**官方结果**：

由于多线圈更多在临床使用，所以官方仅仅给出他们多线圈结果（多线圈的SSIM 4倍和8倍都是最高的），官方不参加比赛。 

SSIM scores are: **多线圈4x (FAIR/NYU SSIM = 0.9301)** and **多线圈8x (FAIR/NYU SSIM = 0.9056)** .

**挑战结果**：

本次比赛一共34个队伍。每组SSIM 排名前五的，专家组根据信噪比、伪影、清晰度、诊断置信度和整体图像质量进行比较。

- Patrick Putzky of the University of Amsterdam (single-coil 4x acceleration)

- Puyang Wang of United Imaging Intelligence (multi-coil 4x) 

- Nicola Pezzotti of Philips (multi-coil 8x) 

  ![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191204023822.png)

**源码**：

已经有几个组提交了代码。

**新闻**：

纽约大学朗格健康中心的放射学系系主任Recht将于12月5日，在北美放射学会在芝加哥举行的年度会议上，介绍更多关于挑战赛的详细信息。

## 3. Organizers and Advisors

- Facebook AI Research: Nafissa Yakubova, Tullie Murrell, Anuroop Sriram, Jure Zbontar, Mike Rabbat, Larry Zitnick
- NYU Langone Health: Florian Knoll, Daniel Sodickson
- Imperial College London: Daniel Rueckert
- Stanford University: Frank Ong
- Berkeley University: Jon Tamir
- Apple Inc.: Joseph Cheng

## 4. Public leaderboard & Challenge leaderboard

Public leaderboards 可以允许公众提交结果来和其他人比较。但是Public leaderboards的提交不计入比赛，结果和程序也不会被官方审核。同时，PL可以使用额外的数据集，但是在提交时要回答是否使用了NYU_DATA之外的额外数据。

![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191204015643.png)



**References**

[^1]: Mark Tygert and Jure Zbontar. Simulating single-coil MRI from the responses of multiple coils. *arXiv preprint*, 2018.
[^2]: Emmanuel J Cand`es, Justin Romberg, and Terence Tao. Robust uncertainty principles: Exact signal reconstruction from highly incomplete frequency information. *IEEE Transactions on Information Theory*, 52(2), 2006.
[^3]: Michael Lustig, David Donoho, and John M Pauly. Sparse MRI: The Application of Compressed Sensing for Rapid MR Imaging. *Magnetic Resonance in Medicine*, 58(6), 2007.



