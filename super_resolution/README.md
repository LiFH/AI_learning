# super resolution
超分辨率问题一直是一个很热门的研究领域，近来随着深度学习的发展，single image super resolution（SISR）也得到迅速的发展。

超分辨率按照是否有匹配的patch可以分为监督学习和非监督学习。

## 监督学习

### upsampling

按照上采样（upsampling）的位置可以将超分网络分为四大类：Pre-upsampling SR、Post-upsampling、Progressive Upsampling SR、Iterative Up-and-Down Sampling SR

#### Pre-upsampling SR

##### SRCNN

C. Dong, C. C. Loy, K. He, and X. Tang, “Learning a deep convolutional network for image super-resolution,” in ECCV,2014.

##### Memnet

​	Y. Tai, J. Yang, X. Liu, and C. Xu, “Memnet: A persistent memory network for image restoration,” in ICCV, 2017.

##### DRRN

​	Y. Tai, J. Yang, and X. Liu, “Image super-resolution via deep recursive residual network,” in CVPR, 2017

##### DRCN

J. Kim, J. Kwon Lee, and K. Mu Lee, “Deeply-recursive convolutional network for image super-resolution,” in CVPR, 2016.

##### ZSSR

​	A. Shocher, N. Cohen, and M. Irani, “zero-shot super-resolution using deep internal learning,” in CVPR, 2018

#### Post-upsampling SR

##### FSRCNN

​	C. Dong, C. C. Loy, and X. Tang, “Accelerating the super- resolution convolutional neural network,” in ECCV, 2016.

##### ESPCN

​	W. Shi, J. Caballero, F. Huszar, J. Totz, A. P. Aitken, R. Bishop, ´D. Rueckert, and Z. Wang, “Real-time single image and video super-resolution using an efficient sub-pixel convolutional neural network,” in CVPR, 2016.

##### SRGAN

​	C. Ledig, L. Theis, F. Huszar, J. Caballero, A. Cunningham, ´ A. Acosta, A. P. Aitken, A. Tejani, J. Totz, Z. Wang et al., “Photo-realistic single image super-resolution using a generative adver-sarial network,” in CVPR, 2017.

##### EDSR

​	B. Lim, S. Son, H. Kim, S. Nah, and K. M. Lee, “Enhanced deep residual networks for single image super-resolution,CVPRW,2017.

##### SRDenseNet

​	T. Tong, G. Li, X. Liu, and Q. Gao, “Image super-resolution using dense skip connections,” in ICCV, 2017

##### DSRN

​	W. Han, S. Chang, D. Liu, M. Yu, M. Witbrock, and T. S. Huang, “Image super-resolution via dual-state recurrent networks,”in CVPR, 2018



#### Progressive Upsampling SR

##### LapSRN

​	W.-S. Lai, J.-B. Huang, N. Ahuja, and M.-H. Yang, “Deep laplacian pyramid networks for fast and accurate superresolution, in CVPR, 2017.

##### MS-LapSRN

​	W.-S. Lai, J.-B. Huang, N. Ahuja, and M.-H. Yang, “Fast and accurate image super-resolution with deep laplacian pyramid networks,” TPAMI, 2018.

##### ProSR

​	Y. Wang, F. Perazzi, B. McWilliams, A. Sorkine-Hornung, O. Sorkine-Hornung, and C. Schroers, “A fully progressive approach to single-image super-resolution,” in CVPRW, 2018.



#### Iterative Up-and-Down Sampling SR
##### DBPN

​	M. Haris, G. Shakhnarovich, and N. Ukita, “Deep backp-rojection networks for super-resolution,” in CVPR, 2018.

##### SRFBN

​	 "Feedback Network for Image Super-Resolution，" in CVPR,2019. 

### Network Design

#### Residual Learning
##### Global Residual Learning

​		J. Kim, J. Kwon Lee, and K. Mu Lee, “Accurate image super resolution using very deep convolutional networks,” in CVPR,2016.
​		Y. Tai, J. Yang, X. Liu, and C. Xu, “Memnet: A persistent memory network for image restoration,” in ICCV, 2017.
​		Y. Tai, J. Yang, and X. Liu, “Image super-resolution via deep recursive residual network,” in CVPR, 2017.
​		Z. Hui, X. Wang, and X. Gao, “Fast and accurate single image super-resolution via information distillation network,” in CVPR,2018.

##### Local Residual Learning

​		Y. Zhang, K. Li, K. Li, L. Wang, B. Zhong, and Y. Fu, “Image super-resolution using very deep residual channel attention networks,” in ECCV, 2018.
​		X. Mao, C. Shen, and Y.-B. Yang, “Image restoration using very deep convolutional encoder-decoder networks with symmetric skip connections,” in NIPS, 2016.
​		W. Han, S. Chang, D. Liu, M. Yu, M. Witbrock, and T. S. Huang, “Image super-resolution via dual-state recurrent networks,” in CVPR, 2018
​		K. He, X. Zhang, S. Ren, and J. Sun, “Deep residual learning for image recognition,” in CVPR, 2016.
​		J. Li, F. Fang, K. Mei, and G. Zhang, “Multi-scale residual network for image super-resolution,” in ECCV, 2018.

#### Recursive Learning

​	to achieve large receptive field and learn higher-level features 

##### DRCN
​		J. Kim, J. Kwon Lee, and K. Mu Lee, “Deeply-recursive convolutional network for image super-resolution,” in CVPR, 2016.

##### DRRN
​		Y. Tai, J. Yang, and X. Liu, “Image super-resolution via deep recursive residual network,” in CVPR, 2017.

##### MemNet
​		Y. Tai, J. Yang, X. Liu, and C. Xu, “Memnet: A persistent memory network for image restoration,” in ICCV, 2017.

##### CARN
​		N. Ahn, B. Kang, and K.-A. Sohn, “Fast, accurate, and lightweight super-resolution with cascading residual network,” in ECCV,2018.

#### Multi-path Learning
##### Global Mutil-path Learning

​		W.-S. Lai, J.-B. Huang, N. Ahuja, and M.-H. Yang, “Deep laplacian pyramid networks for fast and accurate superresolution,” in CVPR, 2017.
​		W. Han, S. Chang, D. Liu, M. Yu, M. Witbrock, and T. S. Huang, “Image super-resolution via dual-state recurrent networks,” in CVPR, 2018.
​		R. Dahl, M. Norouzi, and J. Shlens, “Pixel recursive super resolution,” in ICCV, 2017.

​		H. Ren, M. El-Khamy, and J. Lee, “Image super resolution based on fusing multiple convolution neural networks,” in CVPRW, 2017.

##### Local Mutil-path Learning

​		J.Li,F.Fang,K.Mei,andG.Zhang,“Multi-scaleresidualnetwork for image super-resolution,” in ECCV, 2018.
​	Scale-specific Multi-path Learning
​		B. Lim, S. Son, H. Kim, S. Nah, and K. M. Lee, “Enhanced deep residualnetworksforsingleimagesuper-resolution,”inCVPRW, 2017.
​		N.Ahn,B.Kang,andK.-A.Sohn,“Fast,accurate,andlightweight super-resolution with cascading residual network,” in ECCV, 2018.
​		Y. Wang, F. Perazzi, B. McWilliams, A. Sorkine-Hornung, O. Sorkine-Hornung, and C. Schroers, “A fully progressive approach to single-image super-resolution,” in CVPRW, 2018.

#### Dense Connections
​	G. Huang, Z. Liu, L. Van Der Maaten, and K. Q. Weinberger, “Densely connected convolutional networks,” in CVPR, 2017.
​	T. Tong, G. Li, X. Liu, and Q. Gao, “Image super-resolution using dense skip connections,” in ICCV, 2017.
​	Y. Tai, J. Yang, X. Liu, and C. Xu, “Memnet: A persistent memory network for image restoration,” in ICCV, 2017.
​	N.Ahn,B.Kang,andK.-A.Sohn,“Fast,accurate,andlightweight super-resolution with cascading residual network,” in ECCV, 2018.
​	Y. Zhang, Y. Tian, Y. Kong, B. Zhong, and Y. Fu, “Residual dense network for image super-resolution,” in CVPR, 2018.
​	X. Wang, K. Yu, S. Wu, J. Gu, Y. Liu, C. Dong, C. C. Loy, Y. Qiao, and X. Tang, “Esrgan: Enhanced super-resolution generative adversarial networks,” in ECCV Workshop, 2018.
​	M.Haris,G.Shakhnarovich,andN.Ukita,“Deepback projection networks for super-resolution,” in CVPR, 2018.

#### Channel Attention
​	Y. Zhang, K. Li, K. Li, L. Wang, B. Zhong, and Y. Fu, “Image super-resolution using very deep residual channel attention networks,” in ECCV, 2018.
​	J. Hu, L. Shen, and G. Sun, “Squeeze-and-excitation networks,” in CVPR, 2018.

#### Advanced Convolution
​	Dilated Convolution
​		K. Zhang, W. Zuo, S. Gu, and L. Zhang, “Learning deep cnn denoiser prior for image restoration,” in CVPR, 2017.
​	Group Convolution
​		A. G. Howard, M. Zhu, B. Chen, D. Kalenichenko, W. Wang, T. Weyand, M. Andreetto, and H. Adam, “Mobilenets: Efﬁcient convolutional neural networks for mobile vision applications,” Arxiv:1704.04861, 2017.
​		X. Zhang, X. Zhou, M. Lin, and J. Sun, “Shufﬂenet: An extremely efﬁcient convolutional neural network for mobile devices,” in CVPR, 2018.
​		S. Xie, R. Girshick, P. Doll´ar, Z. Tu, and K. He, “Aggregated residual transformations for deep neural networks,” in CVPR, 2017.
​		N.Ahn,B.Kang,andK.-A.Sohn,“Fast,accurate,and light weight super-resolution with cascading residual network,” in ECCV, 2018.

#### Pixel Recursive Learning
​	R. Dahl, M. Norouzi, and J. Shlens, “Pixel recursive super resolution,” in ICCV, 2017.
​		A. van den Oord, N. Kalchbrenner, L. Espeholt, O. Vinyals, A. Graves et al., “Conditional image generation with pixelcnn decoders,” in NIPS, 2016.
​	Q. Cao, L. Lin, Y. Shi, X. Liang, and G. Li, “Attention-aware face hallucination via deep reinforcement learning,” in CVPR, 2017.
​		J. Najemnik and W. S. Geisler, “Optimal eye movement strategies in visual search,” Nature, vol. 434, 2005.

#### Pyramid Pooling

​	H.Zhao,J.Shi,X.Qi,X.Wang,andJ.Jia,“Pyramidsceneparsing network,” in CVPR, 2017.
​		K. He, X. Zhang, S. Ren, and J. Sun, “Spatial pyramid pooling in deep convolutional networks for visual recognition,” in ECCV, 2014

#### Wavelet Transformation（小波变换）
​	W. Bae, J. J. Yoo, and J. C. Ye, “Beyond deep residual learning for image restoration: Persistent homology-guided manifold simplification,” in CVPRW, 2017.
​	T. Guo, H. S. Mousavi, T. H. Vu, and V. Monga, “Deep wavelet prediction for image super-resolution,” in CVPRW, 2017.
​	H. Huang, R. He, Z. Sun, T. Tan et al., “Wavelet-srnet: A wavelet-based cnn for multi-scale face super resolution,” in ICCV, 2017.
​	P. Liu, H. Zhang, K. Zhang, L. Lin, and W. Zuo, “Multi-level wavelet-cnn for image restoration,” in CVPRW, 2018. 

#### blind sr



## 非监督学习

* Zero-shot Super-resolution

  A. Shocher, N. Cohen, and M. Irani, “zero-shot super-resolution using deep internal learning,” in CVPR, 2018.

* Weakly-supervised Super-Resolution
  	Learned Degradation
  	A. Bulat, J. Yang, and G. Tzimiropoulos, “To learn image super resolution,use a gan to learn how to do image degradation ﬁrst,” in ECCV, 2018

* Cycle-in-cycle Super-resolution
  	Y. Yuan, S. Liu, J. Zhang, Y. Zhang, C. Dong, and L. Lin, “Unsupervised image super-resolution using cycle-in-cycle generative adversarial networks,” in CVPRW, 2018.

* Deep Image Prior
   D. Ulyanov, A. Vedaldi, and V. Lempitsky, “Deep image prior,” in CVPR, 2018.

