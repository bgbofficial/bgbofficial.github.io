---
layout: post
title: Writing@01_w10_Discussion
date: 2019-11-12
tag: Writing
mathjax: true

---

# Writing Journal

Zhiwen Wang, 2019323040005, College of Computer Science, Sichuan University

# Week 5 Target journal

## 1. Task

目标期刊的选择（表格）

<font size=2>Table 1. Rating preferred journals in terms of key criteria for maximizing your publication success.</font>

| Journal name                                              | Recent publication of similar work and novelty               | Match of scope and recent content to your work | Page charges or Open Access costs                            | Time to publication             | impact         |
| --------------------------------------------------------- | ------------------------------------------------------------ | ---------------------------------------------- | ------------------------------------------------------------ | ------------------------------- | -------------- |
| 1. IEEE TRANSACTIONS ON MEDICAL IMAGING (IEEE TMI)        | ENGINEERING, BIOMEDICAL;<br/><br/>ENGINEERING, ELECTRICAL & ELECTRONIC;<br/><br/>RADIOLOGY, NUCLEAR MEDICINE & MEDICAL IMAGING;<br/><br/>COMPUTER SCIENCE, INTERDISCIPLINARY APPLICATIONS;<br/><br/>IMAGING SCIENCE & PHOTOGRAPHIC TECHNOLOGY; | MEDICAL IMAGING                                | Free(Page charge $250 for overlength<br/>manuscripts or color figures)<br/>Above 10 pages | Average 5.4months<br/>(Monthly) | 7.816          |
| 2. IEEE TRANSACTIONS ON IMAGE PROCESSING (IEEE TIP)       | COMPUTER SCIENCE, SOFTWARE, GRAPHICS, PROGRAMMING;<br/><br/>COMPUTER SCIENCE, THEORY & METHODS;<br/><br/>ENGINEERING, ELECTRICAL & ELECTRONIC;<br/><br/>COMPUTER SCIENCE, SOFTWARE ENGINEERING;<br/><br/>COMPUTER SCIENCE, ARTIFICIAL INTELLIGENCE; | COMPUTER SCIENCE, THEORY & METHODS;            | Free(pay all overlength page charges $250,<br/>color charges, and any other charges and fees associated with publication of<br/>the manuscript) Above 10 pages | Average 8.1months<br/>(Monthly) | 6036/889=6.790 |
| 3. MEDICAL IMAGE ANALYSIS(MIA)                            | COMPUTER SCIENCE, ARTIFICIAL INTELLIGENCE;<br/><br/>COMPUTER SCIENCE, INTERDISCIPLINARY APPLICATIONS;<br/><br/>ENGINEERING, BIOMEDICAL;<br/><br/>RADIOLOGY, NUCLEAR MEDICINE & MEDICAL IMAGING; | RADIOLOGY, NUCLEAR MEDICINE & MEDICAL IMAGING; | Free(charge  $250 for Open access and offprints color figure) | (8 issues/year)<br/>5.4 months  | 1918/216=8.880 |
| 4. IEEE TRANSACTIONS ON BIOMEDICAL ENGINEERING<br/>(TBME) | ENGINEERING, BIOMEDICAL                                      | ENGINEERING, BIOMEDICAL                        | Free(charges $250 , such as: overlength  7 pages, OA)        | 3.0 months                      | 2470/550=4.491 |



# Week 6 Writing schedule

## 1. Task

期末提交的文章写作类型，可预计的困难和解决方案，写作时间安排.

## 2. Target journal

目标期刊：Medical Image Analysis or IEEE Transactions On Medical Imaging（两者都是川大计算机学科B区、影响因子分别为8.880和7.816，属于计算机医学图像领域顶刊）

![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/11.png)

<font size=2>Figure 1. 目标期刊在川大分级目录的表格</font>

## 3. Writing schedule

期末提交的文章写作类型：Article;

预计困难和解决方案：预计困难：语法上符合该期刊标准、术语单词是否准确、方法创新度、Introduction的总结精炼程度；解决方案：多收集CNS和目标期刊的句子语法词汇，专业创新度上由导师把关，其他非学术的部分，如Introduction也是多总结课堂上学习的或期刊上看到的句子。

写作时间安排：11月完成Introduction部分，甚至一些思路；

# Week 7 Introduction

## 1. Task

读5篇及以上顶刊或目标期刊的文章introduction部分，并写下自己对该部分在contents/logic/language几方面的阅读收获和体会。

## 2. Gaining

Overview：通过阅读文章，然后看了一些教程，我发现：Introduction 部分要**简单明白，逻辑性强，层层递进，三者紧密结合**。下面来对contents/logic/language展开讨论。郭老师结合常用的写作顺序：先Introduction，后Methods、Results、Discussion、Reference，最后才Abstract、Title，作业也按写作的次序来，这周是Introduction。

Content：Introduction 的内容就是论文的研究背景以及引出，内容要简单易懂，用自己的话说出来。1）在写之前，要确定自己的**创新点**。这些东西需要**逻辑提纲**来连接，这一步可以减少写作时间，写之前确保要和导师沟通；2）写的时候，紧紧围绕过去**研究的缺陷**来描写，清晰地对自己的研究来阐述怎么**解决这些缺陷**。提出自己的工作时，不要拔高自己，**贬低**别人。论文的论点不要太广，抓住一个**重点**来深入，论述太广会让文章重点不够突出。

Logic：从很久“根”研究，可以从时间线出发（如：古典力学 → 近代力学 → 现代物理），也可以从学科的不同逻辑线发展。

Language：衔接词与从句要得体，多用英语习惯的句式，会连贯很多。

## 3. Introduction 五重奏🎶

**具体例子**🌰：

这里以一篇笔者方向的论文 *A Deep Cascade of Convolutional Neural Networks for MR Image Reconstruction.* 作为介绍，希望这个思路是正确的。

1）🎵首先提出研究领域：核磁共振的图像重建（采集原始数据到构成图像的过程叫重建）。In many clinical scenarios, medical imaging is an indispensable diagnostic and research tool. One such important modality is Magnetic Resonance Imaging (MRI), which is non-invasive and offers excellent resolution with various contrast mechanisms to reveal different properties of the underlying anatomy.  （**指出研究范围**）

2）🎵然后，回顾了核磁共振的发展历史，指出了核磁共振成像慢的通病。同时也提出了各个方法提出来解决这个问题。但是这个问题仍然存在，当在动态磁共振当中，这个问题尤为突出，目前的核磁共振成像时间依旧是个问题。However,
MRI is associated with a slow acquisition process. This is because data samples of an MR image are acquired sequentially in k-space and the speed at which k-space can be traversed is limited by underlying MR physics. A long data acquisition procedures impose significant demands on patients, making the tool expensive and less accessible. One possible approach to accelerate the acquisition process is to undersample k-space, which in theory provides an acceleration rate proportional to a reduction factor of a number of k-space traversals required. However, undersampling in k-space violates the Nyquist-Shannon theorem and generates aliasing artefacts when the image is reconstructed. The main challenge in this case is to find an algorithm that takes into account the undersampling undergone and can compensate missing data with a-priori knowledge on the image to be reconstructed. 

Using Compressed Sensing (CS), images can be reconstructed from subNyquist sampling, assuming the following:  ··· ··· Using Compressed Sensing (CS), images can be reconstructed from subNyquist sampling, assuming the following:  ··· ··· （**说明了研究背景，提出存在的一个问题**）

3）🎵随后，介绍深度学习 Deep learning，并指出DL作为MRI重建技术存在的优势。Recently, deep learning has been successful at tackling many computer vision
problems.   ··· ···（**确定研究目标，指出本研究目标的优势**）

4）🎵而后，指出自己课题组前期在 Deep learning 作为核磁图像重建的工作，并由此引出 Deep learning 在核磁共振图像重建领域并未广泛研究。（**指出自己课题组相关的工作，并提出这些工作仍然存在问题或者局限**）

5）🎵最后，提出本文的研究重点是 Deep learning 在图像重建领域的一些发现。结合字典学习和深度学习，能实现核磁共振图像短时间成像，并且有高的图像质量。（**提出本文研究的重点，采用的方法，得出结论**）

**References**

Schlemper, Jo, Jose Caballero, Joseph V. Hajnal, Anthony Price, and Daniel Rueckert. 2017. “A Deep Cascade of Convolutional Neural Networks for MR Image Reconstruction.” In *Information Processing in Medical Imaging*, edited by Marc Niethammer, Martin Styner, Stephen Aylward, Hongtu Zhu, Ipek Oguz, Pew-Thian Yap, and Dinggang Shen, 647–58. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-319-59050-9_51.



# Week 8 Results 

## 1. Task

【第八周学习任务】大家好，本周学习内容如下：
1、Writing Journal. 阅读自己选定文章的Results并记录收获和体会，下次上课带上。（注：可以参考课程资料"Week 8 Results - 8.Tasks "中的条目来记录，也可自行安排。）
2、主题阅读：Discussion。参考书目如下：
（1）Section 2, chapter 9 (Margaret Cargill & O'Connor Patrick. Writing Scientific Research Articles: Strategy and Steps. 2nd Edition. Wiley-Blackwell. 2013.)
（2）Chapter 18 (Adrian Wallwork. English for Writing Research Paper (2nd Edition), Springer. 2016）
（3）PP363-378 (Swales J., Feak C. Academic Writing for Graduate Students: Essential Tasks and Skills. Michigan, ELT. 2012)

## 2. Gaining

该写在Material & Method甚至discussion部分的信息罗列在这里。这里是文章的 “心脏” ，如图1，这部分的描写应该尽可能地清晰简明地描述结论。第一种方法是介绍结果，并在正式进入Discussion部分之前，添加一个简短的总结。对于比较直接和简单，并具有连续性的研究型论文，这种写法是非常常见的。第二种方法是先提出一个部分的结果，然后来给出一个总结。接下来再简要讨论下一个部分。 这种方式通常用于较长的论文，而且接下来的Discussion部分也会遵循相同的结构。

![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191211051959.png)

Figure 1. A type structure of article.

**千万不要简单罗列图标**。这里笔者注意到Results部分给出太多的信息， “too much information”。Results部分不以任何方式解释结果，这部分应该在Discussion里呈现。 Results部分应该尝试不带有任何解释或者评价口气的来叙述发现，而不是直接快速进入Discussion部分。

a）论文撰写Results的要求是翔实准确。准确是结果必须是真实的，不能伪造和篡改；

b）结果提供表和图；

c）Results和Discussion分开写时，Results部分尽量不要涉及对结果的评论，最多是总结陈述结果就可以了；

d）大多要提供统计结果。方差分析的结果形式要根据刊物的格式给出。

对于撰写，清晰目标，准确地传达以目标为核心的数据信息，精确而紧凑的短语和句子是最有效的。在Results部分中进行清晰且令人信服的写作段落，应包括问题，实验方法，结果和小发现（Answer）。

## 3. Results 四重奏 🎶

**具体例子**🌰：

这里以一篇笔者方向的论文 *A Deep Cascade of Convolutional Neural Networks for MR Image Reconstruction.* 作为介绍，希望这个思路是正确的。

1）🎵首先提出问题：通过用简短的句子或短语说明，执行特定实验的目的是要解决什么问题；The means of the reconstruction errors across 10 subjects are summarised in
Table 1. 

2）🎵然后实验方法：在这里，我们不应重复实验细节，建议将方法（尽量简洁明了）与结果联系起来，可使用这两种句型结构模式来阐述：一是使该方法成为句子的主语，二是使用转换短语或句子以及主句中的结果来说明方法。While training CNN is time consuming,
once it is trained, the inference can be done extremely quickly on a GPU.  ··· ···（**这里作者安排在最后一段**）

3）🎵随后结果：结果是关于重要数据的文本描述，并赋予数据意义，同时，得确保是合乎逻辑的。For both 3-fold and 6-fold acceleration, one can see that CNN consistently outperformed DLMRI, and that the standard deviation of the error made by CNN was smaller. The reconstruction from 3-fold acceleration can be found in Fig. 2. It can be seen that the CNN approach produced a smaller overall error. The CNN reconstruction produced a more homogeneous reconstruction. On the other hand, DLMRI gave a blocky reconstruction. In some cases, both CNN and DLMRI suffered from small losses of important anatomical structures in their reconstructions (orange), but CNN was able to recover more details (red). The reconstructions from 6-fold acceleration is in Fig. 3.   

4）🎵最后小发现（Answer）：在最后一个句子中，将该段落的实验结果与问题联系起来，来个小小前后呼应，或引出下一个结果，充当过渡。但这不包括对实验结果的含义的完整讨论。Although both methods suffered from significant loss of structures (orange), CNN was still capable of better preserving the texture than DLMRI (red). On the other hand, DLMRI created extremely block-like artefacts due to over-smoothing. 6× undersampling for these  ··· ···

# Week 10 Discussion 

## 1. Task

【第十周学习任务】大家好，本周学习内容如下：
1、Writing Journal. 阅读选定文章的Discussion并记录收获和体会，下次上课带上。（注：可参考课程资料"Week 10 Discussion - 9.Tasks "中的条目来记录，也可自行安排。）
2、主题阅读：Titile, Abstract, Conclusion。参考书目如下：
（1）Chapter 12, 13, 19 (Adrian Wallwork. English for Writing Research Paper (2nd Edition), Springer. 2016）
（2）Chapter 10, 11 (Margaret Cargill & O'Connor Patrick. Writing Scientific Research Articles: Strategy and Steps. 2nd Edition. Wiley-Blackwell. 2013.)
（3）Unit 5: Writing summaries (Swales J., Feak C. Academic Writing for Graduate Students: Essential Tasks and Skills. Michigan, ELT. 2012)

## 2. Reviewing in class

### How should we structure the Discussion?

The Discussion should answer the following questions, and possibly in the following order. You can thus use the answers to structure your Discussion. This gives you a relatively easy template to follow.

1. What are my most important findings?

2. Do these findings support what I set out to demonstrate at the beginning of the paper?

3. How do my findings compare with that others have found? How consistent are they?

4. What is my personal interpretation of my findings?

5. What other possible interpretations are there?

6. What are the limitations of my study? What other factors could have influenced my findings? Have I reported everything that could make my findings invalid?

7. Do any of the interpretations reveal a possible flaw (i.e. defect, error) in my experiment?

8. Do my interpretations contribute some new understanding of the problem that I have investigated? In which case do they suggest a shortcoming in, or an advance on, the work of others?

9. What external validity do my findings have? How could my findings be generalized to other areas?

10. What possible implications or applications do my findings have? What support can I give for such implications?

11. What further research would be needed to explain the issues raised by my findings? Will I do this research myself or do I want to throw it open to the community?

    

## 7. Good examples

### 7.1 (4)Short discussion

 We have delineated the spatiotemporal dynamics, genomic landscape and functional consequences of naive CD8$^+$ T cells undergoing intrahepatic priming (Extended Data Fig. [10](https://www.nature.com/articles/s41586-019-1620-6#Fig14)). We showed that hepatocellular presentation leads to a CD8$^+$ T cell dysfunction that is distinct from T cell alterations reported in other viral infections and cancer and, as such, is not readily responsive to anti-PD-L1 treatment. As immune checkpoint inhibitors are beginning to be tested in patients persistently infected with HBV, the results reported here should help to interpret the outcome of those studies and eventually inform the design of modified trials in selected cohorts of patients. Our data identify IL-2 as a potent immunotherapeutic that can rescue CD8$^+$ T cells rendered dysfunctional by hepatocellular priming. Thus, IL-2-based strategies should be considered for the treatment of chronic HBV infection. （第一句点题。第二句给出结果。）

\- "Dynamics and genomic landscape of CD8$^+$​ T cells undergoing hepatic priming", *Nature*. 2019-10-08.

短讨论比较注重突出结果，总共有137个单词。

### 7.2 (5)Long discussion

`One striking aspect of our atlas is that`$^{[1][2]}$ the distribution of semantically selective areas is relatively symmetrical across the two cerebral hemispheres. `This finding is inconsistent with`$^{[3]}$ human lesion studies that support the idea that semantic representation is lateralized to the left hemisphere[13](https://www.nature.com/articles/nature17637#ref13). `However`, many fMRI studies of semantic representation find only modest lateralization[1](https://www.nature.com/articles/nature17637#ref1) and one study that used narrative stories found highly bilateral results similar to ours[2](https://www.nature.com/articles/nature17637#ref2). (前面这句话举例出了和自己实验相同和不同的例子)`This suggests that` right hemisphere areas may respond more strongly to narrative stimuli than to the words and short phrases used in most studies. `Still`\*, `more research will be needed to determine` what roles these left- and right-hemisphere semantic areas have in language comprehension.（这句话十分断然，肯定。这是对自己结果的讨论。其中，still这个词语用的很地道和精髓。整个结构是层次递进的：先给出主要发现的结果；然后从不同于人们认为语言的左脑单边侧化--有研究认为适度侧化--有研究认为与他们相似的高度双边侧化；给出讨论，再用Still给出进一步的东西。这一段是主要研究结果的那方面）

`Another interesting aspect of these results is that` the organization of semantically selective brain areas seems to be highly consistent across individuals. `This might suggest` that innate anatomical connectivity or cortical cytoarchitecture constrains the organization of high-level semantic representations[28](https://www.nature.com/articles/nature17637#ref28),[29](https://www.nature.com/articles/nature17637#ref29). `It is also possible that` this is owing to common life experiences of the subjects, all of whom were raised and educated in Western industrial societies. `Future studies that include subjects from more diverse backgrounds will be needed to determine` how much of this organizational consistency reflects innate brain structure versus experience.（might、possible这些词汇的运用，显出这个段落十分缓和，由于没有大规模的调查。这一段是带有猜测的结果的那方面）

`One` `limitation`\*（限制性词语） `of PrAGMATiC as used here is that` each area is assumed to be functionally homogeneous. `This is a common assumption` in the design and analysis of many neuroimaging studies[30](https://www.nature.com/articles/nature17637#ref30). `However`, many cortical maps, including semantic maps in visual cortex[14](https://www.nature.com/articles/nature17637#ref14), `seem to contain` smoothly changing gradients of representation. `It should be possible to modify` the PrAGMATiC algorithm to model functional gradients explicitly. `This will provide an objective tool for determining` whether the semantic maps found here are best described as homogeneous areas or as gradients.（这一段讲局限性。并且说明了原因和可改进方法。注意插入句。从同质性假设谈论到似乎有梯度的不同。提出了修改模型，最后给出试验，做出试验能判断同质模型还是渐变模型好。）

`Data-driven approaches are commonplace in studies of` human neuroanatomy[31](https://www.nature.com/articles/nature17637#ref31) and resting state networks[26](https://www.nature.com/articles/nature17637#ref26),[32](https://www.nature.com/articles/nature17637#ref32), `but`\* `are only beginning to be used`\* in functional imaging[14](https://www.nature.com/articles/nature17637#ref14),[15](https://www.nature.com/articles/nature17637#ref15).` Our study demonstrates` the power and efficiency of data-driven approaches for functional mapping of the human brain. `Although` our experiment used a simple design in which subjects only listened to stories, the data were rich enough to produce a comprehensive atlas of semantically selective areas. `Furthermore`, `our data-driven framework is quite general`\*. Other properties of language can be mapped (even in this same data set) by using feature spaces that reflect phonemes, syntax and so on. Complex semantic models that incorporate information beyond word co-occurrence can be tested and compared quantitatively. `The generalizability of these models can also be tested by` using stimuli beyond autobiographical stories. `It is sometimes difficult to synthesize the results of` data-driven experiments with those from hypothesis-driven experiments, `but future methodological and theoretical developments should help to bridge this divide`\*. `We expect` that the semantic atlas presented here will be useful for many researchers investigating the neurobiological basis of language. We `also` expect that this atlas can be refined and expanded by incorporating results from future studies. `To facilitate this`, we have creatsed a detailed interactive version of the semantic atlas that can be explored online at http://gallantlab.org/huth2016.（结尾段落。第一句总结使用的数据驱动方法在成熟领域和刚发展的领域。but are用的很精髓。紧接着说明了本文的数据驱动方法在这个领域十分好。Although又紧急转折说明了本方法是比较简单的，但很有用。Futhermore，强调了通用性，解释并且举例。此外提出一些该理论是可补充得，并且在将来可以发展：bridge this divide。提出了一些基于此更远研究的希望：We expect，and also expect。区别两者expect的不同。最后给出资源与数据。）

\-  “Natural speech reveals the semantic maps that tile human cerebral cortex,” *Nature*, 2016-04-28.

这篇文章的讨论部分，有三个阅读的好处，总共558个单词。（1）突出了本文第2部分的每个点；（2）跨学科；（3）长讨论。用的好的短语这样标注：`One striking aspect of our atlas is that`$^{[1][2]}$ ，其中[1] [2]指的是在第二节Reviewing in class中对应的讨论方法。用的极好的连词或短语用 \* 星号进行标注：`Still`\*。这些词语与短语都必须进入个人的学术英语写作语料库（因为实在太好用了）。并且在第一段的故事情节是，（1）他们的研究方向；（2）怎么确定这个研究方向的。

## 9. After Class: Tasks

1. Writing Journal. 阅读选定文章的Discussion并记录收获和体会，下次上课带上。（注：可参考课程资料"Week 10 Discussion - 9.Tasks "中的条目来记录，也可自行安排。）

2. 主题阅读：Titile, Abstract, Conclusion。参考书目如下：

   - （1）Chapter 12, 13, 19 (Adrian Wallwork. English for Writing Research Paper (2nd Edition), Springer. 2016
   - （2）Chapter 10, 11 (Margaret Cargill & O'Connor Patrick. Writing Scientific Research Articles: Strategy and Steps. 2nd Edition. Wiley-Blackwell. 2013.)
   - （3）Unit 5: Writing summaries (Swales J., Feak C. Academic Writing for Graduate Students: Essential Tasks and Skills. Michigan, ELT. 2012)  

3. 期末安排
   - week15：提交Final exam
   - week16-17：One On One
   - week18-19：考试，开卷

## 10. Homeworks

### 10.1 Notices that I must do in reading the discussion of a paper

1. Read your selected articles and examine the following questions. What moves can you identify in thr Discussion section? For example:

   - Move1-Backgroud information (research purposes, theory, methodology, optinal);

   - Move2-Summarizing and reporting key results (obligatory);

   - Move3-Commenting on the key results (making claims, explaining the results, comparing the new work with the previous studies, offering alternative explanations);

   - Move4-Stating the limitations of the study (optional, but probable in some fields);

   - Move5-Making recommendations for future implementation and/or for future research (optional);

2. Note the words or phrases of generality. In the Discussion section, a common device is to use one of the following "phrases of generality". For example:

   Overall / In general / On the whole / In the main / With ... exception(s);

   The overall results indicate..., / The results indicate, overall, that..., / With one exception, the experimental samples resisted...

3. Limitations in Discussion. Here are some typical formulations for stating limitations in one's research scope. For example: It should be noted that this study has been primarily concerned with ..., / This analysis has concentrated on ..., / The findings of this study are restricted to ..., /This study has addressed only the question of ...,/ We would like to point out that we have not ...

   Here are some typical openings for statements that firmly state that certain conclusions should not be drawn. For example: However, the findings do not simply...,/ The results of this study cannot be taken as evidence for ...,/ Unfortunately, we are unable to determine from this data ...,/ The lack of ... means that we cannot be certain ...,/ Notwithstanding its limitations, this study does suggest ...,/ Despite its preliminary character, the research reported here would seem to indicate ...,/ However exploratory, this study may offer some insight into ...,/

4. What about the length of sentences in Discussion. Long or short? How many words in long sentences?

### 10.2 The discussion of 1st paper (Nat Mach Intell, Jun. 2019)

The proposed MAP-NN, enhanced by the radiologist in the loop, performs favourably or comparably relative to the clinically used iterative reconstruction methods implemented by the three leading CT vendors. Once the MAP-NN is trained, the DL-based denoising process is highly efficient (about 100 slices per second per mapping depth) and easy to use in clinical practice, while iterative reconstruction techniques are time-consuming and subject to significant artefacts.（不同于 7.2 (5)Long discussion 里面的多个句子的讨论，本文第一段只用了两个句子，而且还是长句。很是奇怪。第一句给出了相比迭代算法的效果，第二句给出了相比的两个优点：速度和伪影。在第一句就提到了radiologist的帮助，证明其作用很大。这段给出了对比于迭代算法的效果。）

Compared to previously published DL-based denoising networks[14](https://www.nature.com/articles/s42256-019-0057-9#ref-CR14),[15](https://www.nature.com/articles/s42256-019-0057-9#ref-CR15),[16](https://www.nature.com/articles/s42256-019-0057-9#ref-CR16),[17](https://www.nature.com/articles/s42256-019-0057-9#ref-CR17),[19](https://www.nature.com/articles/s42256-019-0057-9#ref-CR19),[20](https://www.nature.com/articles/s42256-019-0057-9#ref-CR20),[21](https://www.nature.com/articles/s42256-019-0057-9#ref-CR21),[22](https://www.nature.com/articles/s42256-019-0057-9#ref-CR22),[23](https://www.nature.com/articles/s42256-019-0057-9#ref-CR23), which learn the denoising mapping from images collected at a specific low-dose setting to their NDCT counterparts, our MAP-NN can be viewed as a significant refinement and a major extension that learns not only intermediate denoised images through multiple CLONE stages but also the associated noise reduction direction. The number of CLONE modules, also known as the mapping depth, is a key parameter, and the radiologists have the best judgement regarding the selection of an optimal mapping depth in a task-specific fashion. MAP-NN with CLONEs provides a cost-effective and user-friendly interface between DL and radiologists, enabling mixed/augmented intelligence beyond what standalone DL could achieve. We provide more details about the differences between the conventional denoising model and the proposed progressive denoising model in Supplementary Notes [1](https://www.nature.com/articles/s42256-019-0057-9#MOESM1) and [2](https://www.nature.com/articles/s42256-019-0057-9#MOESM1).（LDCT, Low dose CT，NDCT，Normal dose CT。这段给出了相比之前的神经网络方法的对比。并且说明和之前的NN不同的特点：significant、major。接着具体讲了本文方法的mapping depth导致的不同，马上接上radiologist的帮助是best。马上又强调了MAP-NN的易用性。最后给出了附件细节。这段给出了相比之前的神经网络方法的对比，并给出了一个重要细节，radiologist。）

Our MAP-NN systematically demonstrates that the DL approach can provide a similar or better image quality in terms of structural fidelity and noise suppression as commercial iterative reconstruction (IR)  methods performing image reconstruction directly from raw data. Most importantly for clinical use, the DL approach is computationally much more efficient than IR. The DL approach can thus already effectively compete with IR solutions, and potentially replace the IR approach. Furthermore, because DL methods can be vendor agnostic, institutions that have CT scanners of various brands and from different vendors can utilize the MAP-NN model to produce similar image appearances, which is not possible with commercial IR techniques. Even though all reconstruction and processing algorithms are commercial products, our post-processing algorithm can be embedded within image viewer software, which is independent of any vendor. Currently, unique changes in image appearance are associated with vendor-specific reconstruction programs. This is an obstacle for large-scale radiomics studies, and could be streamlined using DL techniques in the future.（ structural fidelity：结构保真度。这段是对上面两段的总结。也点题目了。第一句直接说明效果，第一句很长。然后讨论了DL方法早已达到IR方法效果。好处：从系统性的优点 $\to$ 临床计算 $\to$ 商业性质。 猜测性词语potentially， 目前的困窘性词语obstacle） 

However, there are some limitations of this study. First, as an overall comparative study, the MAP-NN has not been optimized to either a specific vendor or a particular body region. The collection of more data will help improve the denoising performance and enhance the statistical significance of the denoising gains over the IR results. Second, LDCT and NDCT slices in a testing set may not be in perfect registration, which can affect the evaluation scores to some degree. Finally, our DL method was selected to be applicable to CT scans from all three vendors, from which we cannot have access to raw data. More powerful DL methods cannot be implemented without the data format. Despite these limitations, our overall conclusion has been encouraging that DL is either better than or comparable to IR. In collaboration with a vendor, our algorithm could be specifically trained with their data and achieve an even better performance than what we have described here using our agnostic algorithm. With the availability of raw data, CT denoising can be performed from the sinogram domain to the image space, utilizing all the information for the best denoising results. Clearly, it is now time for CT vendors to open their data format, perform machine learning and develop the next generation of CT image reconstruction algorithms in the DL framework.（这段给出了限制，说明是通用性的东西，需要特定厂家和特定部位的优化以及更多数据，给出方法。keyword： However 。 Despite ，转折，说明限制也是死限制的限制。通篇强调了厂家与数据，说明限制是可以破除的。 Clearly，呼吁）registration：配准

In conclusion, our DL method provides better or similar image quality compared to commercial IR techniques from three CT vendors, and there is great potential for optimizing DL-based CT reconstruction methods that handle sinogram data directly.（directly）

\-  “Competitive performance of a modularized deep neural network compared to commercial algorithms for low-dose CT image reconstruction,” *Nat Mach Intell*, vol. 1, no. 6, pp. 269–276, Jun. 2019.

 artefacts: 伪影。

### 10.3 The discussion of 2nd paper (Nat Biomed Eng, Nov. 2019)

To better understand the deep-learning model, we analyse the semantic representations learned from the model. Generally speaking, successful generation of volumetric images is possible only if the model is able to learn the semantic representation of the 3D structure from the input projections. Thus, for the same volume, the representations obtained via learning from different angular projections should be similar, since they describe the same underlying 3D scene. In Fig. [6a](https://www.nature.com/articles/s41551-019-0466-4#Fig6), we visualize the feature maps extracted from the transformation module for two testing samples. For visualization purposes, only 5 randomly chosen channels among the 4,096 feature maps are shown, each with a size of 4 × 4 pixels. The feature maps learned from different numbers of 2D projections are displayed separately in different columns. The results show that, when different 2D views are given, the model extracts similar semantic representations of the underlying 3D scene. Furthermore, Fig. [6b](https://www.nature.com/articles/s41551-019-0466-4#Fig6) shows the visualization of *t*-distributed stochastic neighbour embedding (*t*-SNE) for the feature maps of 15 testing samples. The *t*-SNE technique is commonly used to visualize high-dimensional data by embedding each sample as a point in a 2D space[38](https://www.nature.com/articles/s41551-019-0466-4#ref-CR38). The four points in a cluster of the same colour represent the learned features from one-, two-, five- and ten-view reconstructions. The figure shows clustering behaviour for feature maps from the same sample, indicating that the model learns a similar representation from different 2D projections.

We also measure the similarity of the embedding representations by calculating the Euclidean distance between two feature maps. In this way, we compute a similarity score, ranging from 0 to 1, where high similarity (a score approaching 1) indicates that the distance between two feature maps is close to zero. We plot a correlation matrix (Fig. [6c](https://www.nature.com/articles/s41551-019-0466-4#Fig6)) among 50 randomly selected testing samples, with their feature representations extracted from one-view and two-view reconstruction models. The highest values stand out in the diagonal of the correlation matrix whereas other off-diagonal values remain relatively low. This illustrates that the two sets of feature representations learned from one-view and two-view projections for the same 3D scene are more similar or closer in Euclidean distance space compared with the feature representations learned from other different 3D scenes. This provides additional evidence supporting the capability of the model to learn a semantic representation of the 3D scene with a single projection.

Robustness against possible irregular breathing patterns is important for future clinical implementation of the approach. The robustness of deep networks against various perturbations is an intense area of research in artificial intelligence[39](https://www.nature.com/articles/s41551-019-0466-4#ref-CR39),[40](https://www.nature.com/articles/s41551-019-0466-4#ref-CR40),[41](https://www.nature.com/articles/s41551-019-0466-4#ref-CR41),[42](https://www.nature.com/articles/s41551-019-0466-4#ref-CR42),[43](https://www.nature.com/articles/s41551-019-0466-4#ref-CR43),[44](https://www.nature.com/articles/s41551-019-0466-4#ref-CR44),[45](https://www.nature.com/articles/s41551-019-0466-4#ref-CR45),[46](https://www.nature.com/articles/s41551-019-0466-4#ref-CR46). As summarized in ref. [43](https://www.nature.com/articles/s41551-019-0466-4#ref-CR43), possible solutions come in three categories: (1) the modification of network architectures (for example, adding more layers, changing the loss function and modifying the activation functions); (2) the use of external models as a network add-on to detect out-of-distribution data (for example, using an external detector to rectify the irregular data); and (3) the modification of the training-data distribution or the training strategy (for example, adding regularization, data augmentation or leveraging adversarial training). In (1), the efforts are focused on refining the learning models. In (2), irregular motions might be regarded as out-of-distribution data, where some potential techniques, such as a detector subnetwork[41](https://www.nature.com/articles/s41551-019-0466-4#ref-CR41) or the confidence-based method[42](https://www.nature.com/articles/s41551-019-0466-4#ref-CR42),[44](https://www.nature.com/articles/s41551-019-0466-4#ref-CR44), might be useful for detecting irregular input. Among the various methods, the modification of the training-data distribution is arguably the most straightforward way to proceed. The rationale is that if the irregularities can be incorporated effectively into the training dataset and the training strategy can be adjusted accordingly, the robustness of the trained model would be enhanced. To a certain extent, this has been elaborated in the example in Supplementary Fig. [7](https://www.nature.com/articles/s41551-019-0466-4#MOESM1), where it is demonstrated that, because of the inclusion of augmented training datasets with rotational transformations, the deep-learning approach is much more robust against a small rotation of the imaging subject than a conventional principal component analysis (PCA)-based method. Quantitative results of the study for the testing sample presented in Supplementary Fig. [7](https://www.nature.com/articles/s41551-019-0466-4#MOESM1) are shown in Supplementary Table [1](https://www.nature.com/articles/s41551-019-0466-4#MOESM1).

#### Outlook

We have described a deep-learning approach for volumetric imaging with ultra-sparse data sampling and a patient-specific prior. The data-driven strategy is capable of holistically extracting the feature characteristics embedded in a single projection or in a few 2D projections, and of transforming them into the corresponding 3D image through model learning. The image-feature space transformation plays an essential role in the ultra-sparse image reconstruction. At the training stage, the method incorporates diverse forms of a priori knowledge into the reconstruction. The manifold-mapping function is learned from the training datasets, rather than relying on any ad hoc form of motion trajectory. Although we have used X-ray imaging and patient-specific data, the concept and implementation of the approach could be extended to other imaging modalities or to other data domains with ultra-sparse sampling. Practically, single-view imaging represents a potential solution for many image-guided interventional procedures and may help to simplify the hardware of tomographic imaging systems.

\-  “Patient-specific reconstruction of volumetric computed tomography images from a single projection view via deep learning,” *Nat Biomed Eng*, vol. 3, no. 11, pp. 880–888, Nov. 2019.

评价：这篇文章的discussion写得较为专业术语。

### 10.4 The discussion of 3rd paper (MAI)

Discussions and conclusions

In this paper, we propose a novel method based on the Wasserstein generative adversarial network to remove the Rician noise in MR images while effectively preserving the structural details. This network aims to process 3D volume data using a 3D convolutional neural network. In addition to the introduction of the WGAN framework, there are two more advantages to our method: the innovative generator structure and mixed weighted loss function. The generator is constructed with an autoencoder structure, which symmetrically contains convolutional and deconvolutional layers, aided by a residual structure. Another improvement of our method is the adaptation of the mixed loss function, which combines the MSE and perceptual losses with a weighted form.

The experimental results demonstrate that with the help of WGAN and perceptual loss, the CNN-based method is significantly improved in both qualitative and quantitative aspects. Compared to several state-of-the-art methods, including BM3D, PRI-NLM3D and CNN3D, our proposed RED-WGAN effectively avoids oversmoothing effects while preserving more details. Furthermore, to validate the robustness and generalization of our model, we trained our model with several specific noise levels and tested it on various noise levels. Meanwhile, real noisy clinical data were involved. In both cases, the proposed RED-WGAN model achieved a performance better than the traditional methods in both visual effects and quantitative results.

The computational cost of the deep learning-based method is worth mentioning. The training stage is the costliest step. Although the training procedure is usually performed on the GPU, it is still time-consuming. For our training set, when we alternatingly train the generator and discriminator networks, each epoch takes approximately 40 min. Although other methods, such as BM4D and PRI-NLM3D, do not need to train, their running times are much longer than the DL-based methods. In this paper, the average execution times for the clinical dataset for BM4D, PRI-NLM3D, CNN3D and RED-WGAN were 5.73, 4.16, 0.17 and 0.16 s, respectively. In practice, the running time for DL-based methods can be further reduced by using GPU for testing.

In conclusion, the results obtained in the paper are encouraging and efficiently demonstrate the potential of deep learning-based methods for MRI denoising. In the future, instead of training on a specific noise level, we will try to extend our method to a more general form for different noise levels. Furthermore, incorporating the image reconstruction method may be interesting.

\- “Denoising of 3D magnetic resonance images using a residual encoder–decoder Wasserstein generative adversarial network,” *Medical Image Analysis*, vol. 55, pp. 165–180, Jul. 2019.

### 10.5  The discussion of 4th paper (TMI)

With the development of CSC in recent years, CSC has been proven useful in many imaging problems, including super-resolution, image fusion, image decomposition and so on. Instead of dividing an image into overlapped patches, CSC directly works on the whole image, which maintains more details and avoids artifacts caused by patch aggregation. In this paper, we propose two methods based on CSC. The basic version introduces CSC into the PWLS reconstruction framework. To further improve the performance and preserve more structural information, gradient regularization on feature maps is imposed into the basic version. Qualitative and quantitative results demonstrate the merits of our methods.

In the experiments of Section IV-A and IV-B, the filters and parameters were the same, showing the generalization of the proposed methods and that there is no need to adjust the filters or the parameters patient by patient. We also examined the impacts of filters on our method. The experimental results show that PWLS-CSCGR can work well even with only four filters. PWLS-CSCGR is also robust to the training set or even without the training set and can be treated as an unsupervised learning method.

Importantly, another issue is the computational time. The main cost of our methods depends on two parts: training the filters and the reconstruction. Training 32 filters with 10 images costs 85 s of GPU. Because this operation is offline and there is no need for a large training set, this part will not be the main problem. On the other hand, the reconstruction is time-consuming. Although our methods have a similar heavy computational burden to PWLS-DL, several techniques, including parallel computing and advanced optimization methods, can be applied for acceleration.

One of the most important deep learning models is CNN, which is also based on the convolution operator. For CSC, a signal can be represented by a summation of convolutions between a set of filters and the corresponding feature maps, and the key point is to calculate the feature maps with certain (predetermined or adaptive) filters. CNN trains the cascaded filters to convolve with the inputs. Furthermore, current CNN-based methods still lack theoretical proof. Most deep learning methods are data-driven, and the results cannot be guaranteed without sufficient training data. However, CSC, as an unsupervised learning method, has a strict mathematical proof. This method is robust to the number of training samples (as shown in Sec. IV-C.3 and IV-C.4) and even without training data. On the other hand, the same groups analyzed the relationship between the CSC and CNN methods in [59], [60] and found that assuming that our signals originate from the multi-layer CSC model, the layered-thresholding pursuit algorithm for decomposing a given measurement vector $Y$ completely equals the forward propagation in CNNs. This interesting finding provides a new way to explore the interpretability of deep learning.

In conclusion, inspired by successful applications of CSC in the field of signal processing, we explored the potential of this method incorporating a PWLS image reconstruction framework, resulting in two novel algorithms referred to as PWLS-CSC and PWLS-CSCGR. We evaluated the proposed algorithms with simulated and real data. In the experimental results, our methods have been shown to be competitive with several state-of-art methods. The robustness of our methods was also investigated by extensive analysis with experimental configurations. In our future work, we will extend our methods to other CT imaging topics, such as metal artifact reduction and LDCT. Furthermore, the combination with deep learning-based methods is also an interesting direction.

\- “Convolutional Sparse Coding for Compressed Sensing CT Reconstruction,” *IEEE Transactions on Medical Imaging*, pp. 1–1, 2019.

评价：以上两篇论文discussion写得十分专业，经常使用术语和方法细节。

## Reference

[1] A. G. Huth, W. A. de Heer, T. L. Griffiths, F. E. Theunissen, and J. L. Gallant, “Natural speech reveals the semantic maps that tile human cerebral cortex,” *Nature*, vol. 532, no. 7600, pp. 453–458, Apr. 2016.

[2] H. Shan *et al.*, “Competitive performance of a modularized deep neural network compared to commercial algorithms for low-dose CT image reconstruction,” *Nat Mach Intell*, vol. 1, no. 6, pp. 269–276, Jun. 2019.

# Week 11  Title and Abstract 

## 1. Task

【第11周学习任务】大家好，本周学习内容如下：
1、Writing Journal. 阅读选定文章的Title和Abstract并记录收获和体会。（注：可参考课程资料"Week 11 - Task 1&2 "来记录）
2、主题阅读：Review & Language Focus。后三本书可在library genesis下载。
（1）Chapter 4/5/6/10/11 (Adrian Wallwork. English for Writing Research Paper (2nd Edition), Springer. 2016）
（2）Part 2 （The text，Karen Englander, Writing and publishing science research papers in English: A global perspective）
（3）整本浏览，约90页（Feak C & Swales, J., 2009, Telling a research story: writing a literature review）
（4）Chapter 11 （Diana Ridley 2012, The literature review: a step-by-step guide for students）

## 2. Gainings of Abstract

a）背景（2-3句）

介绍背景，研究目标。

b）方法（2-3句）

简要写出，主要是整体设计。

c）结果（3-4句）

如果没有必要，不要使用特定值。这里是对results的总结和概括。

d）结论（1-2句）

重新引入背景，解释为什么论文的结果很重要。论文重要性经常会在Intro，Abstract，Disccussion中讨论。

## 3. Abstract 四重奏 🎶

**具体例子**🌰：

这里以一篇笔者方向的论文 *A Deep Cascade of Convolutional Neural Networks for MR Image Reconstruction.* 作为介绍，希望这个思路是正确的。

1）🎵首先背景：The acquisition of Magnetic Resonance Imaging (MRI) is inherently slow.  

2）🎵然后方法：Inspired by recent advances in deep learning, we propose a framework for reconstructing MR images from undersampled data using a deep cascade of convolutional neural networks to accelerate the data acquisition process.  

3）🎵随后结果：We show that for Cartesian undersampling of 2D cardiac MR images, the proposed method outperforms the state-of-the-art compressed sensing approaches, such as dictionary learning-based MRI (DLMRI) reconstruction, in terms of reconstruction error, perceptual quality and reconstruction speed for both 3-fold and 6-fold undersampling. Compared to DLMRI, the error produced by the method proposed is approximately twice as small, allowing to preserve anatomical structures more faithfully.  

4）🎵最后结论：Using our method, each image can be reconstructed in 23 ms, which is fast enough to enable real time applications.  

## 4. Gainings of Title

这个题目将被成千上万的人阅读。也许很少有人会阅读整篇论文，但许多人会在原始期刊，二级（摘要和索引）数据库，搜索引擎输出等其他方面阅读标题。因此，标题中的所有单词都应谨慎选择，并且必须谨慎管理彼此之间的关联。

目前，好Title的定义为：充分描述论文核心内容的所用单词最少的组合。

在作者的领域，应该是很好起标题，一般是提出一种方法，然后给它命名，介绍是在核磁共振图像重建领域就行：

A Deep Cascade of Convolutional Neural
Networks for MR Image Reconstruction  

Image reconstruction by domain-transform
manifold learning  

Scan‐specific robust artificial‐neural‐networks for k‐space
interpolation (RAKI) reconstruction: Database‐free deep
learning for fast imaging  