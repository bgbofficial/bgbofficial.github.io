---
 []
layout: post
title: MRI@04_DyMriReconDL
date: 2019-11-19
tag: MRI
mathjax: true

---

# A Brief Review of Deep Learning Reconstruction of Dynamic Magnetic  Resonance Imaging

Zhiwen Wang, 2019323040005, College of Computer Science, Sichuan University

# *ABSTRACT*

Computer vision and image processing have been revolutionized by deep learning (DL) techniques recently. The main purpose of this paper is to review and summarize the emerging research work of deep learning of dynamic magnetic resonance imaging (DMRI). After the brief introduction of deep learning techniques and conventional MRI, the applicaiton of DL in MRI and DMRI are reviwed mainly from two aspects: approaches using deep learning techniques end-to-end, tackled by a combination of deep learning with other techniques. In addition, an summary neartly three years on DL-based DMRI has been conducted. Finally, some new trends of DL-based DMRI are discussed.

#  Ⅰ. INTRODUCTION

Computer vision and image processing have been revolutionized by deep learning (DL) [^9] techniques recently. It  refers to feed the net of DL a set of images as inputs and generate feature maps of these images as inputs. Still, the DL-based tied is sweeping over the area of clinic and health. In clinic application, magnetic resonance imaging (MRI) is used in revealing a organic or pathological lesion,  diagnosis and  treatment monitoring [^10], offering a non-invasive imaging method being perhaps its most essential characteristic. The technology produces a high-definition anatomical images. Dynamic magnetic resonance imaging (DMRI), it is a continuous multi-frame magnetic resonance imaging of the same targets, which contains time and space information, attempting to trace the activities of organs [^11] and the process of medicine transportation[^12], such as, cardiovascular imaging [^13] and perfusion imaging [^14]. Unfortunately, because of hardware and physiological constraints [^15], reconstruction speed on MRI is generally limited, restrained by Nyquist sampling theory, and the repercussions of such limitations proven even more serious in DMRI (see Figure 1) [^16]. Furthermore, artefacts incurred often by involuntary organ movements due to breathing, heartbeat, etc. make DMRI faces a serious challenge. Meanwhile, the DL outburst for imaging proceeding provides a good opportunities for improvements of the DMRI spatio-temporal correlation. 

![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191211101853.png)

<font size=2> Figure 1. The MRI acquisition process is not fast enough to take
fully sampled snapshots in real-time. Instead, data is acquired over
multiple heartbeats, and a compressed sensing theory reconstruction is used to suppress
image artifacts caused by sub-Nyquist sampling.  </font>

In this brief survey, recent uses of DL to solve imaging reconstruction problems in DMRI are summarized and discussed. 

## A. RELATED WORKS

### 1) MRI

In MRI, images are reconstructed from raw data acquired
in the Fourier domain.  If an image’s Fourier data is fully  sampled (i.e. sampled at the Nyquist rate), then the image
can be linearly reconstructed without aliasing artifacts with
a simple 2-D Fourier transform while a image reconstructed from a undersampled data with artefacts (see Figure 2).  

Over the last years, different research have offered a large set of new tools in order to shorten the acquisition times that are essential to reconstruct  a complete MRI [^1]. Of which, the compressed sensing theory (CS) [^21] [^22] [^23] [^24] plays the most important role in reducing MRI time as CS theory holds that reconstructing high quality MR images promptly from partial samples, which is far less Nyquist sampling theory. Specifically, a appropriate pick of sparse transform model, which includes short time Fourier transform, temporal total variation, dictionary learning, CS joint low rank approximation methods, etc. [^16] [^26] [^27] [^28] [^29], is important to CS-based MRI [^25]. But actually, using optimization based approaches above, researchers have troubled in two long existing problems that how to select a correct regularization functions and their hyper-parameter is the first and reconstruction on the slow speed is the second. 

On the contrary, deep learning attempts to learn hierarchical features and rules from data with a fast deploying speed after training period. Convolutional Neural Networks (CNN) (see Figure 3) and Recurrent neural networks (RNN)-based, more generally deep learning, on MRI reconstruction methods is amazingly growing, began, in 2016, with Wang et al [^2] and Yang et al [^3]. 

![1](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191211103444.png)

<font size=2> Figure 2. The  contrast between fully sampled MR image and unfully sampled MR image using conventional method to reconstruct.  </font>

![1](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1576042352738&di=ca7b0ca3ffce01377c7b4be9ce135e41&imgtype=0&src=http%3A%2F%2Fneuralnetworksanddeeplearning.com%2Fimages%2Ftikz40.png)

<font size=2> Figure 3. A type of CNN.  </font>

Specifically, Wang et al [^2] developed a specialized CNN, augmenting a conventional compressed-sensing reconstruction with a regularizer, and Yang et al [^3] given undersampled $k$-space data as inputs to their nets and reconstructions from fully sampled $k$-space data as outputs. A recent research by Chen et al [^6] proposed a variational networks, which has been used to single-shot fast spin-echo MRI with different sampling rates. This approach reduced the time of image reconstruction, reached to 200 ms per section, outperforming the best traditional parallel imaging and compressed sensing reconstruction. And, other DL-based methods have been investigated to reduce artefacts and accelerate speed in MRI, such as long short-term memory (LSTM), generative adversarial networks (GAN), CNN-stimulating some estimation, such as optical flow estimation, and etc [^70] [^71] [^72] [^73].

### 2) DYNAMIC MRI

For conventional DMRI, there are various approaches which are applied to accelerate DMRI and create a better quality DMRI, such as CS-theory [^74] [^75], TV [^76], motion estimation, dictionary learning and so on [^77] [^78], in order to exploit the spatio-temporal correlations in the process of DMRI.

However, in deep learning methods, how to model a DMRI has been little researched so far, only a few did it from the angle of dynamic reconstruction which includes DC-CNN [^5], GDLSM [^18], CRNN [^19], ME-CNN [^20], CNN-based [^30] , etc.. Hence, deep learning reconstruction of dynamic MRI is a new researching form, which exits many problems that are worth to exploring and making exercise. Besides, a key in dynamically reconstructing is to best utilize spatio-temporal redundancy when modeling a deep learning approach to DMRI [^4]. 

Significantly, a deep cascade of CNN (DC-CNN), by Schlemper et al [^7], inspired by iterative reconstruction of DL-based methods, has been successfully applied to stimulated the iterative reconstruction of dictionary learning-based methods in 2017, recognized as a milestone to DL- based DMRI. Furthermore, in same year, same team extended the DC-CNN method [^5] to reconstruct  real-time MRI (23 ms per image frame) independently and dynamically adapt the temporal parameter of cine MRI according to learn spatio-temporal correlations and redundancies efficiently by combining convolution and data sharing approaches. In particular, the success of DC-CNN is also related to very powerful augmentation techniques that include, for example, flexible and rigid deformations. A 2018 deep learning work [^4] shows improvement in dynamic MRI reconstruction over convolutional recurrent neural networks-based methods, which reconstructs good quality cardiac cine MRI from partial $k$-space data by considering simultaneously spatio-temporal dependencies. In the paper, they show that this largely outperforms CNN-based and compressed sensing approaches used in dynamic MRI reconstruction algorithms in term of computational complexity, accuracy and speed of reconstruction for different undersampled data. This October, the current widely-accepted state-of-the-art is the end-to-end-trainable motion-estimating convolutional neural network (ME-CNN) [^20], which is comprised of three components: motion estimation network, data-consistent motion-augmented cine (DC-MAC) and 3D CNN, presenting a approach to exploit the full temporal information of the $k$-space raw data while DC-CNN do not give sufficient consideration on these information.

In addition, many different structures of CNN-based [^31] ~ [^55] were evaluated empirically in their reconstruction. For example, based on DC-CNN, Qin et al [^39] proposed a novel net named $k-t$ NEXT to research spatio-temporal correlations. Their optimal configuration verified empirically has been presented in Table 1.  

<font size=2>Table 1. A short list of DL-DMRI</font>

| Architectures    |                       Proposed Models                        |                           Features                           |
| :--------------- | :----------------------------------------------------------: | :----------------------------------------------------------: |
| CNN              | Deep cascade of convolutional neural networks (DC-CNN) [^5]  | Proposing the concepts of data consistency and data sharing spiked by the iterative reconstruction of dictionary learning; learning spatio-temporal prior knowledge |
| CNN, RNN         |     Convolutional Recurrent Neural Networks (CRNN) [^4]      | CRNN block implicitly learning iterative denoising interleaved by data consistency layers to enforce data fidelity |
| CNN              | Motion-estimating convolutional neural network (ME-CNN) [^20] | Exploiting more spatio-temporal information than DC-CNN; learning spatio-temporal prior knowledge |
| CNN              |  Dilated multi-level densely connected network (mDCN) [^31]  | Combining linear subspace modeling and deep learning methods, replacing nonlinear manifold modeling, in special conditions; learning spatio-temporal prior knowledge |
| CNN              | DynamIc MR imaging method with both k-spacE aNd Spatial prior knowledge integrated via muItI-supervised netwOrk traiNing: DIMENSION [^32] | Learning spatio-temporal prior knowledge by muitI-supervised |
| CNN, RNN         |  Motion-guided dynamic reconstruction network (MODRN) [^33]  | Capturing motion information inspired by a optical flow estimation work [^60] [^61] |
| CNN              |                Deep self-learning nets [^34]                 | self-learning DMRI framework based on denoising auto encoders (DAE) |
| CNN              | Model‐based deep learning - SmooThness regularization on manifolds: MoDL-SToRM  [^35] | Synergizing CNN and complementary image regularization penalties; learning spatio-temporal prior knowledge |
| CNN, RNN, GAN    |                   GAN-RNN-CNN-Based [^36]                    | Learning knowledge by some high-dimensional combination, generating by CRNN and GAN |
| CNN              |   A DC-CNN architecture with weighted loss function [^37]    | Altering the DC-CNN loss function to improve the quality of images |
| CNN, U-Net       |                A $k$-space deep network [^38]                | Based on a mathematic finding [^62] and a CNN [^63], the net is applied to $k$-space interpolation for multiple coils. |
| CNN, RNN         |      $k$-t NEtwork with X-f Transform: $k$-t NEXT [^39]      | Inspired by $k-t$ BLAST [^64] and $k-t$ FOCUSS [^65] [^66], the work propose to reconstruct the true signals from aliased signals in x-f domain to exploit the spatio-temporal redundancies, including $X-f$ CNN and CRNN |
| CNN              |              Learn analysis transform net [^40]              | Replacing ADMM with CNN to optimize discrete cosine transform (DCT) in the spatial domain and total variation (TV); Small dataset |
| CNN              |                 A end-to-end CNN [^41][^43]                  |     Reducing artefacts in cine MRI with A end-to-end CNN     |
| CNN              |             The 1st version of MoDL-SToRM [^42]              |    Similar to DC-CNN, but the model reuse the CNN weight.    |
| CNN, ResNet      | Multiple overlapping-4 echoes detachment: Single-shot MOLED-4 [^44] | Based on overlapping echoes detachment (OLED), they proposed a multiple OLED, making a quantitative imaging in DMRI. |
| CNN, U-Net       |            A modified version of the U-net [^45]             | Reducing under-sampling artefacts in cine MRI by a modified U-Net; post processing methods |
| CNN, U-Net, LSTM |             A net based on U-Net and LSTM [^46]              | Exploiting the implicit temporal information of cine MRI; post-processing |
| CNN              |                    A generative CNN[^47]                     | Inspired by a 2018 work [^67],a unsupervised learning model is to map the manifold of latent variables onto a manifold of dynamic images, in which a generative CNN reconstructs DMRI from $k$-space. |
| CNN, DAE         |            A spatial-temporal DEA (ST-DAE) [^48]             | Followed by their DISPEL [^68] in 2017, a modified net named ST-DAE is applied to reduce radial streaking artefacts. |
| CNN              |                Deep Basis Pursuit (DBP) [^49]                | Noise is reduced by a CNN and data consistency layers, taking place of ADMM in $\ell-1$ minimization of basis pursuit. |
| CNN              |              Joint deep learning network [^50]               | The network consist of motion estimation (Motion-Seg Net [^69]) and segmentation jointly, which estimates and segments the cardiac motion from raw data of cine MRI directly; Imaging analysis |
| GAN              |                     A general GAN [^51]                      | A GAN network, trained by a dataset from UK Biobank, produce MRIs forming a piece of cine from $k$-space data. |
| Cycle-GAN        |         Standard plane synthesis GAN (SPSGAN) [^53]          | Inspired by a work [^52] and based on Cycle-GAN [^55], this work expanded their previous research [^54],  which produce high quality cine MRIs in the assessment of cardiac function. |

## B. DISCUSSION AND FUTURE WORK

In this paper, we have provided a systematic overview of the state-of-the-art DL-based DMRI.  

It is clear that convolutional neural networks are useful in practice when a net is applied to generate satisfactory outputs, trained completely by complicated datasets. Only local patterns can be learned by CNN, as a means of data-driven, but it remains to be seen how to imaging more complicated texture and shape in images [^5]. Meanwhile, some researchers argued the outputs may be interfered by a new type of deep learning artefacts [^56]. But some researchers, who have tried deep learning approaches in medical imaging, including computed tomography (CT) reconstruction and MRI, are optimistic that the DL methods will be implemented in medical imaging reconstruction in the future [^57] [^58] [^59]. 

Based on the discussion above all, the deep learning issues easily are divided into the following categories: 1) proceeding without deep learning components at all; 2) a combination of deep learning and other methods; 3) Full usage of deep learning. Also, these approaches using deep learning can be broken down into three camps  (see Figure4) : 1) image-domain learning; 2) k-space or data-domain learning, *e.g.,* RAKI; 3) transform learning (direct from k-space to image), *e.g.,* AUTOMAP; 4) hybrid-domain learning (unrolled loop, e.g., variational network) that alternate between denoising/dealiasing and reconstruction from k-space, *e.g.,* DC-CNN, ME-CNN.

![4](https://wzwimg-1300620626.cos.ap-chengdu.myqcloud.com/githubimg/clipboard_20191211111220.png)

<font size=2> Figure 4. Deep learning reconstruction in DMRI. a) image-domain learning; b) k-space or data-domain learning ; c) transform learning ; d) hybrid-domain learning .</font>

Besides, some research trends and potential future research directions are given as follows: 

- *Utilization of different undersampling patterns* : most of all reconstruct DMRI using Cartesian undersampling data, and other sampling methods should be investigated in the future, such as radial spiral trajectories [^5]. In addition, multiple coil data from parallel MRI should be used to more research in DMRI with DL for speeding up the acquisition [^4].

- *Optimization of undersampling mask* : deep learning techniques, especially deep neural networks, have been regarded as black boxes models. The implicit mechanism of DL maybe optimises the undersampling mask with DL [^5].

- *Exploring other memory units* : some spatio-temporal information is stored in a network containing RNN components. Researchers can explore other memory units, such as GRU and LSTM [^4]. 

- *More efficient CNN architectures* : some researchers argued that more efficient CNN-based architectures should be explored for a better performance in terms of imaging quality, computational complexity and time complexity [^20] [^31].

It is believed that deep learning will have a more and more prospective future impacting MRI, especially in DMRI.

# ACKNOWLEDGEMENTS

I would like to thank Dr. Guo Xia for her writing courses and helpful insights over the course of this *project*.

# REFERENCES

[^1]: Tsao, Jeffrey. 2010. “Ultrafast Imaging: Principles, Pitfalls, Solutions, and Applications.” *Journal of Magnetic Resonance Imaging* 32 (2): 252–66. https://doi.org/10.1002/jmri.22239.
[^2]: Wang, Shanshan, Zhenghang Su, Leslie Ying, Xi Peng, Shun Zhu, Feng Liang, Dagan Feng, and Dong Liang. 2016. “Accelerating Magnetic Resonance Imaging via Deep Learning.” In *2016 IEEE 13th International Symposium on Biomedical Imaging (ISBI)*, 514–17. https://doi.org/10.1109/ISBI.2016.7493320.
[^3]: Yang, yan, Jian Sun, Huibin Li, and Zongben Xu. 2016. “Deep ADMM-Net for Compressive Sensing MRI.” In *Advances in Neural Information Processing Systems 29*, edited by D. D. Lee, M. Sugiyama, U. V. Luxburg, I. Guyon, and R. Garnett, 10–18. Curran Associates, Inc. http://papers.nips.cc/paper/6406-deep-admm-net-for-compressive-sensing-mri.
[^4]: Qin, Chen, Jo Schlemper, Jose Caballero, Anthony N. Price, Joseph V. Hajnal, and Daniel Rueckert. 2019. “Convolutional Recurrent Neural Networks for Dynamic MR Image Reconstruction.” *IEEE Transactions on Medical Imaging* 38 (1): 280–90. https://doi.org/10.1109/TMI.2018.2863670.
[^5]: Schlemper, Jo, Jose Caballero, Joseph V. Hajnal, Anthony N. Price, and Daniel Rueckert. 2018. “A Deep Cascade of Convolutional Neural Networks for Dynamic MR Image Reconstruction.” *IEEE Transactions on Medical Imaging* 37 (2): 491–503. https://doi.org/10.1109/TMI.2017.2760978.
[^6]: Chen, Feiyu, Valentina Taviani, Itzik Malkiel, Joseph Y. Cheng, Jonathan I. Tamir, Jamil Shaikh, Stephanie T. Chang, Christopher J. Hardy, John M. Pauly, and Shreyas S. Vasanawala. 2018. “Variable-Density Single-Shot Fast Spin-Echo MRI with Deep Learning Reconstruction by Using Variational Networks.” *Radiology* 289 (2): 366–73. https://doi.org/10.1148/radiol.2018180445.
[^7]: Schlemper, Jo, Jose Caballero, Joseph V. Hajnal, Anthony Price, and Daniel Rueckert. 2017. “A Deep Cascade of Convolutional Neural Networks for MR Image Reconstruction.” In *Information Processing in Medical Imaging*, edited by Marc Niethammer, Martin Styner, Stephen Aylward, Hongtu Zhu, Ipek Oguz, Pew-Thian Yap, and Dinggang Shen, 647–58. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-319-59050-9_51..
[^8]: Knoll, Florian, Kerstin Hammernik, Erich Kobler, Thomas Pock, Michael P. Recht, and Daniel K. Sodickson. 2019. “Assessment of the Generalization of Learned Image Reconstruction and the Potential for Transfer Learning.” *Magnetic Resonance in Medicine* 81 (1): 116–28. https://doi.org/10.1002/mrm.27355.
[^9]: LeCun, Yann, Yoshua Bengio, and Geoffrey Hinton. 2015. “Deep Learning.” *Nature* 521 (7553): 436–44. https://doi.org/10.1038/nature14539.
[^10]: Edelman, Robert R, and Steven Warach. 1993. “Magnetic Resonance Imaging.” *New England Journal of Medicine* 328 (10): 708–16. https://doi.org/10.1056/NEJM199303113281008.
[^11]: Kwong, K. K., J. W. Belliveau, D. A. Chesler, I. E. Goldberg, R. M. Weisskoff, B. P. Poncelet, D. N. Kennedy, B. E. Hoppel, M. S. Cohen, and R. Turner. 1992. “Dynamic Magnetic Resonance Imaging of Human Brain Activity during Primary Sensory Stimulation.” *Proceedings of the National Academy of Sciences* 89 (12): 5675–79. https://doi.org/10.1073/pnas.89.12.5675.
[^12]: Kim, Hyuncheol, Michael R. Robinson, Martin J. Lizak, Ginger Tansey, Robert J. Lutz, Peng Yuan, Nam S. Wang, and Karl G. Csaky. 2004. “Controlled Drug Release from an Ocular Implant: An Evaluation Using Dynamic Three-Dimensional Magnetic Resonance Imaging.” *Investigative Ophthalmology & Visual Science* 45 (8): 2722–31. https://doi.org/10.1167/iovs.04-0091.
[^13]: Edelman, R R, H P Mattle, D J Atkinson, T Hill, J P Finn, C Mayman, M Ronthal, H M Hoogewoud, and J Kleefield. 1990. “Cerebral Blood Flow: Assessment with Dynamic Contrast-Enhanced T2*-Weighted MR Imaging at 1.5 T.” *Radiology* 176 (1): 211–20. https://doi.org/10.1148/radiology.176.1.2353094.
[^14]: Covarrubias, Diego J., Bruce R. Rosen, and Michael H. Lev. 2004. “Dynamic Magnetic Resonance Perfusion Imaging of Brain Tumors.” *The Oncologist* 9 (5): 528–37. https://doi.org/10.1634/theoncologist.9-5-528.
[^15]: Feng, Li, Thomas Benkert, Kai Tobias Block, Daniel K. Sodickson, Ricardo Otazo, and Hersh Chandarana. 2017. “Compressed Sensing for Body MRI.” *Journal of Magnetic Resonance Imaging* 45 (4): 966–87. https://doi.org/10.1002/jmri.25547.
[^16]: Wang, Yang, Ning Cao, Zuojun Liu, and Yudong Zhang. 2017. “Real-Time Dynamic MRI Using Parallel Dictionary Learning and Dynamic Total Variation.” *Neurocomputing* 238 (May): 410–19. https://doi.org/10.1016/j.neucom.2017.01.083.
[^17]: Wang, Ge, Jong Chu Ye, Klaus Mueller, and Jeffrey A. Fessler. 2018. “Image Reconstruction Is a New Frontier of Machine Learning.” *IEEE Transactions on Medical Imaging* 37 (6): 1289–96. https://doi.org/10.1109/TMI.2018.2833635.
[^18]: Batenkov, Dmitry, Yaniv Romano, and Michael Elad. 2017. “On the Global-Local Dichotomy in Sparsity Modeling.” In *Compressed Sensing and Its Applications: Second International MATHEON Conference 2015*, edited by Holger Boche, Giuseppe Caire, Robert Calderbank, Maximilian März, Gitta Kutyniok, and Rudolf Mathar, 1–53. Applied and Numerical Harmonic Analysis. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-319-69802-1_1.
[^19]: Qin, Chen, Jo Schlemper, Jose Caballero, Anthony N. Price, Joseph V. Hajnal, and Daniel Rueckert. 2019. “Convolutional Recurrent Neural Networks for Dynamic MR Image Reconstruction.” *IEEE Transactions on Medical Imaging* 38 (1): 280–90. https://doi.org/10.1109/TMI.2018.2863670.
[^20]: Seegoolam, Gavin, Jo Schlemper, Chen Qin, Anthony Price, Jo Hajnal, and Daniel Rueckert. 2019. “Exploiting Motion for Deep Learning Reconstruction of Extremely-Undersampled Dynamic MRI.” In *Medical Image Computing and Computer Assisted Intervention – MICCAI 2019*, edited by Dinggang Shen, Tianming Liu, Terry M. Peters, Lawrence H. Staib, Caroline Essert, Sean Zhou, Pew-Thian Yap, and Ali Khan, 704–12. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-32251-9_77.
[^21]: Lustig, Michael, David Donoho, and John M. Pauly. 2007. “Sparse MRI: The Application of Compressed Sensing for Rapid MR Imaging.” *Magnetic Resonance in Medicine* 58 (6): 1182–95. https://doi.org/10.1002/mrm.21391.
[^22]: Lustig, Michael, David L. Donoho, Juan M. Santos, and John M. Pauly. 2008. “Compressed Sensing MRI.” *IEEE Signal Processing Magazine* 25 (2): 72–82. https://doi.org/10.1109/MSP.2007.914728.
[^23]: Gamper, Urs, Peter Boesiger, and Sebastian Kozerke. 2008. “Compressed Sensing in Dynamic MRI.” *Magnetic Resonance in Medicine* 59 (2): 365–73. https://doi.org/10.1002/mrm.21477.
[^24]: Feng, Li, Thomas Benkert, Kai Tobias Block, Daniel K. Sodickson, Ricardo Otazo, and Hersh Chandarana. 2017. “Compressed Sensing for Body MRI.” *Journal of Magnetic Resonance Imaging* 45 (4): 966–87. https://doi.org/10.1002/jmri.25547.
[^25]: Liu, Fan, Dongxiao Li, Xinyu Jin, Wenyuan Qiu, Qi Xia, and Bin Sun. 2019. “Dynamic Cardiac MRI Reconstruction Using Motion Aligned Locally Low Rank Tensor (MALLRT).” *Magnetic Resonance Imaging*, July. https://doi.org/10.1016/j.mri.2019.07.002.
[^26]: Caballero, Jose, Daniel Rueckert, and Joseph V. Hajnal. 2012. “Dictionary Learning and Time Sparsity in Dynamic MRI.” In *Medical Image Computing and Computer-Assisted Intervention – MICCAI 2012*, edited by Nicholas Ayache, Hervé Delingette, Polina Golland, and Kensaku Mori, 256–63. Lecture Notes in Computer Science. Berlin, Heidelberg: Springer. https://doi.org/10.1007/978-3-642-33415-3_32.
[^27]: Caballero, Jose, Anthony N. Price, Daniel Rueckert, and Joseph V. Hajnal. 2014. “Dictionary Learning and Time Sparsity for Dynamic MR Data Reconstruction.” *IEEE Transactions on Medical Imaging* 33 (4): 979–94. https://doi.org/10.1109/TMI.2014.2301271.
[^28]: Otazo, Ricardo, Daniel Kim, Leon Axel, and Daniel K. Sodickson. 2010. “Combination of Compressed Sensing and Parallel Imaging for Highly Accelerated First-Pass Cardiac Perfusion MRI.” *Magnetic Resonance in Medicine* 64 (3): 767–76. https://doi.org/10.1002/mrm.22463.
[^29]: Yao, Jiawen, Zheng Xu, Xiaolei Huang, and Junzhou Huang. 2018. “An Efficient Algorithm for Dynamic MRI Using Low-Rank and Total Variation Regularizations.” *Medical Image Analysis* 44 (February): 14–27. https://doi.org/10.1016/j.media.2017.11.003.
[^30]: Sandino, Christopher M, Neerav Dixit, Joseph Y Cheng, and Shreyas S Vasanawala. n.d. “Deep Convolutional Neural Networks for Accelerated Dynamic Magnetic Resonance Imaging,” 8.
[^31]: Chen, Yuhua, Jaime L. Shaw, Yibin Xie, Debiao Li, and Anthony G. Christodoulou. 2019. “Deep Learning Within a Priori Temporal Feature Spaces for Large-Scale Dynamic MR Image Reconstruction: Application to 5-D Cardiac MR Multitasking.” In *Medical Image Computing and Computer Assisted Intervention – MICCAI 2019*, edited by Dinggang Shen, Tianming Liu, Terry M. Peters, Lawrence H. Staib, Caroline Essert, Sean Zhou, Pew-Thian Yap, and Ali Khan, 495–504. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-32245-8_55.
[^32]: Wang, Shanshan, Ziwen Ke, Huitao Cheng, Sen Jia, Ying Leslie, Hairong Zheng, and Dong Liang. 2018. “DIMENSION: Dynamic MR Imaging with Both K-Space and Spatial Prior Knowledge Obtained via Multi-Supervised Network Training.” *ArXiv:1810.00302 [Cs]*, November. http://arxiv.org/abs/1810.00302.
[^33]: Huang, Qiaoying, Dong Yang, Hui Qu, Jingru Yi, Pengxiang Wu, and Dimitris N. Metaxas. 2018. “Dynamic MRI Reconstruction with Motion-Guided Network.” In . https://openreview.net/forum?id=Bke-CJtel4.
[^34]: Ahmed, Abdul Haseeb, Hemant Aggarwal, Prashant Nagpal, and Mathews Jacob. 2019. “Dynamic MRI Using Deep Manifold Self-Learning.” *ArXiv:1911.02492 [Eess]*, November. http://arxiv.org/abs/1911.02492.
[^35]: Biswas, Sampurna, Hemant K. Aggarwal, and Mathews Jacob. 2019. “Dynamic MRI Using Model-Based Deep Learning and SToRM Priors: MoDL-SToRM.” *Magnetic Resonance in Medicine* 82 (1): 485–94. https://doi.org/10.1002/mrm.27706.
[^36]: Jeyaraj, Pandia Rajan, and Edward Rajan Samuel Nadar. n.d. “High-Performance Dynamic Magnetic Resonance Image Reconstruction and Synthesis Employing Deep Feature Learning Convolutional Networks.” *International Journal of Imaging Systems and Technology* n/a (n/a). Accessed November 22, 2019. https://doi.org/10.1002/ima.22381.
[^37]: Jeelani, Haris, Jonathan Martin, Francis Vasquez, Michael Salerno, and Daniel S. Weller. 2018. “Image Quality Affects Deep Learning Reconstruction of MRI.” In *2018 IEEE 15th International Symposium on Biomedical Imaging (ISBI 2018)*, 357–60. https://doi.org/10.1109/ISBI.2018.8363592.
[^38]: Cha, Eunju, Eung Yeop Kim, and Jong Chul Ye. 2018. “Improved Time-Resolved MRA Using k-Space Deep Learning.” In *Machine Learning for Medical Image Reconstruction*, edited by Florian Knoll, Andreas Maier, and Daniel Rueckert, 47–54. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-00129-2_6.
[^39]: Qin, Chen, Jo Schlemper, Jinming Duan, Gavin Seegoolam, Anthony Price, Joseph Hajnal, and Daniel Rueckert. 2019. “K-t NEXT: Dynamic MR Image Reconstruction Exploiting Spatio-Temporal Correlations.” In *Medical Image Computing and Computer Assisted Intervention – MICCAI 2019*, edited by Dinggang Shen, Tianming Liu, Terry M. Peters, Lawrence H. Staib, Caroline Essert, Sean Zhou, Pew-Thian Yap, and Ali Khan, 505–13. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-32245-8_56.
[^40]: Wang, Shanshan, Yanxia Chen, Taohui Xiao, Ziwen Ke, Qiegen Liu, and Hairong Zheng. 2019. “LANTERN: Learn Analysis Transform Network for Dynamic Magnetic Resonance Imaging with Small Dataset.” *ArXiv:1908.09140 [Cs, Eess]*, August. http://arxiv.org/abs/1908.09140.
[^41]: Tamada, Daiki, Marie-Luise Kromrey, Hiroshi Onishi, and Utaroh Motosugi. 2018. “Method for Motion Artifact Reduction Using a Convolutional Neural Network for Dynamic Contrast Enhanced MRI of the Liver.” *ArXiv:1807.06956 [Cs]*, October. http://arxiv.org/abs/1807.06956.
[^42]: Biswas, Sampurna, Hemant K. Aggarwal, Sunrita Poddar, and Mathews Jacob. 2018. “Model-Based Free-Breathing Cardiac MRI Reconstruction Using Deep Learned Storm Priors: MODL-STORM.” In *2018 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)*, 6533–37. https://doi.org/10.1109/ICASSP.2018.8462637.
[^43]: Tamada, Daiki, Marie-Luise Kromrey, Shintaro Ichikawa, Hiroshi Onishi, and Utaroh Motosugi. 2019. “Motion Artifact Reduction Using a Convolutional Neural Network for Dynamic Contrast Enhanced MR Imaging of the Liver.” *Magnetic Resonance in Medical Sciences* advpub. https://doi.org/10.2463/mrms.mp.2018-0156.
[^44]: Zhang, Jun, Jian Wu, Shaojian Chen, Zhiyong Zhang, Shuhui Cai, Congbo Cai, and Zhong Chen. 2019. “Robust Single-Shot T2 Mapping via Multiple Overlapping-Echo Acquisition and Deep Neural Network.” *IEEE Transactions on Medical Imaging* 38 (8): 1801–11. https://doi.org/10.1109/TMI.2019.2896085.
[^45]: Kofler, Andreas, Marc Dewey, Tobias Schaeffter, Christian Wald, and Christoph Kolbitsch. 2019. “Spatio-Temporal Deep Learning-Based Undersampling Artefact Reduction for 2D Radial Cine MRI with Limited Data.” *IEEE Transactions on Medical Imaging*, 1–1. https://doi.org/10.1109/TMI.2019.2930318.
[^46]: Basty, Nicolas, and Vicente Grau. 2018. “Super Resolution of Cardiac Cine MRI Sequences Using Deep Learning.” In *Image Analysis for Moving Organ, Breast, and Thoracic Images*, edited by Danail Stoyanov, Zeike Taylor, Bernhard Kainz, Gabriel Maicas, Reinhard R. Beichel, Anne Martel, Lena Maier-Hein, et al., 23–31. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-00946-5_3.
[^47]: Jin, Kyong Hwan, Harshit Gupta, Jerome Yerly, Matthias Stuber, and Michael Unser. 2019. “Time-Dependent Deep Image Prior for Dynamic MRI.” *ArXiv:1910.01684 [Cs, Eess]*, October. http://arxiv.org/abs/1910.01684.
[^48]: Suzuki, Yudai, Keigo Kawaji, Amit R. Patel, Satoshi Tamura, and Satoru Hayamizu. 2017. “Toward Effective Noise Reduction for Sub-Nyquist High-Frame-Rate MRI Techniques with Deep Learning.” In *2017 Asia-Pacific Signal and Information Processing Association Annual Summit and Conference (APSIPA ASC)*, 1136–39. https://doi.org/10.1109/APSIPA.2017.8282197.
[^49]: Tamir, Jonathan I., Stella X. Yu, and Michael Lustig. 2019. “Unsupervised Deep Basis Pursuit: Learning Inverse Problems without Ground-Truth Data.” *ArXiv:1910.13110 [Eess]*, October. http://arxiv.org/abs/1910.13110.
[^50]: Qin, Chen, Wenjia Bai, Jo Schlemper, Steffen E. Petersen, Stefan K. Piechnik, Stefan Neubauer, and Daniel Rueckert. 2018. “Joint Motion Estimation and Segmentation from Undersampled Cardiac MR Image.” In *Machine Learning for Medical Image Reconstruction*, edited by Florian Knoll, Andreas Maier, and Daniel Rueckert, 55–63. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-00129-2_7.
[^51]: Oksuz, Ilkay, James Clough, Aurelien Bustin, Gastao Cruz, Claudia Prieto, Rene Botnar, Daniel Rueckert, Julia A. Schnabel, and Andrew P. King. 2018. “Cardiac MR Motion Artefact Correction from K-Space Using Deep Learning-Based Reconstruction.” In *Machine Learning for Medical Image Reconstruction*, edited by Florian Knoll, Andreas Maier, and Daniel Rueckert, 21–29. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-00129-2_3.
[^52]: Dar, Salman UH., Mahmut Yurt, Levent Karacan, Aykut Erdem, Erkut Erdem, and Tolga Çukur. 2019. “Image Synthesis in Multi-Contrast MRI With Conditional Generative Adversarial Networks.” *IEEE Transactions on Medical Imaging* 38 (10): 2375–88. https://doi.org/10.1109/TMI.2019.2901750.
[^53]: Zhang, Le, Marco Pereañez, Christopher Bowles, Stefan K. Piechnik, Stefan Neubauer, Steffen E. Petersen, and Alejandro F. Frangi. 2019. “Unsupervised Standard Plane Synthesis in Population Cine MRI via Cycle-Consistent Adversarial Networks.” In *Medical Image Computing and Computer Assisted Intervention – MICCAI 2019*, edited by Dinggang Shen, Tianming Liu, Terry M. Peters, Lawrence H. Staib, Caroline Essert, Sean Zhou, Pew-Thian Yap, and Ali Khan, 660–68. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-32245-8_73.
[^54]: Zhang, Le, Ali Gooya, Marco Pereañez, Bo Dong, Stefan K. Piechnik, Stefan Neubauer, Steffen E. Petersen, and Alejandro F. Frangi. 2019. “Automatic Assessment of Full Left Ventricular Coverage in Cardiac Cine Magnetic Resonance Imaging With Fisher-Discriminative 3-D CNN.” *IEEE Transactions on Biomedical Engineering* 66 (7): 1975–86. https://doi.org/10.1109/TBME.2018.2881952.
[^55]: Gatys, Leon A., Alexander S. Ecker, and Matthias Bethge. 2016. “Image Style Transfer Using Convolutional Neural Networks.” The IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2016, pp. 2414-2423. http://openaccess.thecvf.com/content_cvpr_2016/html/Gatys_Image_Style_Transfer_CVPR_2016_paper.html.
[^56]: Huang, Yixing, Tobias Würfl, Katharina Breininger, Ling Liu, Günter Lauritsch, and Andreas Maier. 2018. “Some Investigations on Robustness of Deep Learning in Limited Angle Tomography.” In *Medical Image Computing and Computer Assisted Intervention – MICCAI 2018*, edited by Alejandro F. Frangi, Julia A. Schnabel, Christos Davatzikos, Carlos Alberola-López, and Gabor Fichtinger, 145–53. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-00928-1_17.
[^57]: Shan, Hongming, Atul Padole, Fatemeh Homayounieh, Uwe Kruger, Ruhani Doda Khera, Chayanin Nitiwarangkul, Mannudeep K. Kalra, and Ge Wang. 2019. “Competitive Performance of a Modularized Deep Neural Network Compared to Commercial Algorithms for Low-Dose CT Image Reconstruction.” *Nature Machine Intelligence* 1 (6): 269–76. https://doi.org/10.1038/s42256-019-0057-9.
[^58]: Wang, Ge, Jong Chu Ye, Klaus Mueller, and Jeffrey A. Fessler. 2018. “Image Reconstruction Is a New Frontier of Machine Learning.” *IEEE Transactions on Medical Imaging* 37 (6): 1289–96. https://doi.org/10.1109/TMI.2018.2833635.
[^59]: Kim, Jonghoon, Jisu Hong, and Hyunjin Park. 2018. “Prospects of Deep Learning for Medical Imaging,” June. https://pr.ibs.re.kr/handle/8788114/5466.
[^60]: Ren, Zhe, Junchi Yan, Bingbing Ni, Bin Liu, Xiaokang Yang, and Hongyuan Zha. 2017. “Unsupervised Deep Learning for Optical Flow Estimation.” In *Thirty-First AAAI Conference on Artificial Intelligence*. https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/view/14388.
[^61]: Meister, Simon, Junhwa Hur, and Stefan Roth. 2018. “UnFlow: Unsupervised Learning of Optical Flow With a Bidirectional Census Loss.” In *Thirty-Second AAAI Conference on Artificial Intelligence*. https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/view/16502.
[^62]: Ye, Jong Chul., Yoseob. Han, and Eunju. Cha. 2018. “Deep Convolutional Framelets: A General Deep Learning Framework for Inverse Problems.” *SIAM Journal on Imaging Sciences* 11 (2): 991–1048. https://doi.org/10.1137/17M1141771.
[^63]: Jin, Kyong Hwan, Dongwook Lee, and Jong Chul Ye. 2016. “A General Framework for Compressed Sensing and Parallel MRI Using Annihilating Filter Based Low-Rank Hankel Matrix.” *IEEE Transactions on Computational Imaging* 2 (4): 480–95. https://doi.org/10.1109/TCI.2016.2601296.
[^64]: Tsao, Jeffrey, Peter Boesiger, and Klaas P. Pruessmann. 2003. “K-t BLAST and k-t SENSE: Dynamic MRI with High Frame Rate Exploiting Spatiotemporal Correlations.” *Magnetic Resonance in Medicine* 50 (5): 1031–42. https://doi.org/10.1002/mrm.10611.
[^65]: Jung, Hong, Kyunghyun Sung, Krishna S. Nayak, Eung Yeop Kim, and Jong Chul Ye. 2009. “K-t FOCUSS: A General Compressed Sensing Framework for High Resolution Dynamic MRI.” *Magnetic Resonance in Medicine* 61 (1): 103–16. https://doi.org/10.1002/mrm.21757.
[^66]: Jung, Hong, Jong Chul Ye, and Eung Yeop Kim. 2007. “Improvedk–TBLAST Andk–TSENSE Using FOCUSS.” *Physics in Medicine and Biology* 52 (11): 3201–3226. https://doi.org/10.1088/0031-9155/52/11/018.
[^67]: Ulyanov, Dmitry, Andrea Vedaldi, and Victor Lempitsky. 2018. “Deep Image Prior.” *The IEEE Conference on Computer Vision and Pattern Recognition (CVPR)*, 2018, pp. 9446-9454. http://openaccess.thecvf.com/content_cvpr_2018/html/Ulyanov_Deep_Image_Prior_CVPR_2018_paper.html.
[^68]: Kawaji, Keigo, Mita B. Patel, Charles G. Cantrell, Akiko Tanaka, Marco Marino, Satoshi Tamura, Hui Wang, et al. 2017. “A Fast, Noniterative Approach for Accelerated High‐temporal Resolution Cine‐CMR Using Dynamically Interleaved Streak Removal in the Power‐spectral Encoded Domain with Low‐pass Filtering (DISPEL) and Modulo‐prime Spokes (MoPS).” *Medical Physics* 44 (7): 3450–63. https://doi.org/10.1002/mp.12234.
[^69]: Qin, Chen, Wenjia Bai, Jo Schlemper, Steffen E. Petersen, Stefan K. Piechnik, Stefan Neubauer, and Daniel Rueckert. 2018. “Joint Learning of Motion Estimation and Segmentation for Cardiac MR Image Sequences.” In *Medical Image Computing and Computer Assisted Intervention – MICCAI 2018*, edited by Alejandro F. Frangi, Julia A. Schnabel, Christos Davatzikos, Carlos Alberola-López, and Gabor Fichtinger, 472–80. Lecture Notes in Computer Science. Cham: Springer International Publishing. https://doi.org/10.1007/978-3-030-00934-2_53.
[^70]: Lundervold, Alexander Selvikvåg, and Arvid Lundervold. 2019. “An Overview of Deep Learning in Medical Imaging Focusing on MRI.” *Zeitschrift Für Medizinische Physik*, Special Issue: Deep Learning in Medical Physics, 29 (2): 102–27. https://doi.org/10.1016/j.zemedi.2018.11.002.
[^71]: Maier, Andreas, Christopher Syben, Tobias Lasser, and Christian Riess. 2019. “A Gentle Introduction to Deep Learning in Medical Image Processing.” *Zeitschrift Für Medizinische Physik*, Special Issue: Deep Learning in Medical Physics, 29 (2): 86–101. https://doi.org/10.1016/j.zemedi.2018.12.003.
[^72]: McCann, Michael T., Kyong Hwan Jin, and Michael Unser. 2017. “Convolutional Neural Networks for Inverse Problems in Imaging: A Review.” *IEEE Signal Processing Magazine* 34 (6): 85–95. https://doi.org/10.1109/MSP.2017.2739299.
[^73]: Mazurowski, Maciej A., Mateusz Buda, Ashirbani Saha, and Mustafa R. Bashir. 2019. “Deep Learning in Radiology: An Overview of the Concepts and a Survey of the State of the Art with Focus on MRI.” *Journal of Magnetic Resonance Imaging* 49 (4): 939–54. https://doi.org/10.1002/jmri.26534.
[^74]: Liu, Fan, Dongxiao Li, Xinyu Jin, Wenyuan Qiu, Qi Xia, and Bin Sun. 2019. “Dynamic Cardiac MRI Reconstruction Using Motion Aligned Locally Low Rank Tensor (MALLRT).” *Magnetic Resonance Imaging*, July. https://doi.org/10.1016/j.mri.2019.07.002.
[^75]: Gamper, Urs, Peter Boesiger, and Sebastian Kozerke. 2008. “Compressed Sensing in Dynamic MRI.” *Magnetic Resonance in Medicine* 59 (2): 365–73. https://doi.org/10.1002/mrm.21477.
[^76]: Wang, Yang, Ning Cao, Zuojun Liu, and Yudong Zhang. 2017. “Real-Time Dynamic MRI Using Parallel Dictionary Learning and Dynamic Total Variation.” *Neurocomputing* 238 (May): 410–19. https://doi.org/10.1016/j.neucom.2017.01.083.
[^77]: He, Ning, Ruolin Wang, and Yixue Wang. 2019. “Dynamic MRI Reconstruction Exploiting Blind Compressed Sensing Combined Transform Learning Regularization.” *Neurocomputing*, April. https://doi.org/10.1016/j.neucom.2018.12.087.
[^78]: Godino-Moya, Alejandro, Javier Royuela-del-Val, Muhammad Usman, Rosa-María Menchón-Lara, Marcos Martín-Fernández, Claudia Prieto, and Carlos Alberola-López. 2019. “Space-Time Variant Weighted Regularization in Compressed Sensing Cardiac Cine MRI.” *Magnetic Resonance Imaging* 58 (May): 44–55. https://doi.org/10.1016/j.mri.2019.01.005.

























