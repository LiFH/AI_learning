# super resolution
超分辨率问题一直是一个很热门的研究领域，近来随着深度学习的发展，single image super resolution（SISR）也得到迅速的发展。

超分辨率按照是否有匹配的patch可以分为监督学习和非监督学习。

## 监督学习

### 按照upsampling位置分类

按照上采样（upsampling）的位置可以将超分网络分为四大类：Pre-upsampling SR、Post-upsampling、Progressive Upsampling SR、Iterative Up-and-Down Sampling SR

#### Pre-upsampling SR

* SRCNN

C. Dong, C. C. Loy, K. He, and X. Tang, “Learning a deep convolutional network for image super-resolution,” in ECCV,2014.

* Memnet

​	Y. Tai, J. Yang, X. Liu, and C. Xu, “Memnet: A persistent memory network for image restoration,” in ICCV, 2017.

* DRRN

​	Y. Tai, J. Yang, and X. Liu, “Image super-resolution via deep recursive residual network,” in CVPR, 2017

* DRCN

J. Kim, J. Kwon Lee, and K. Mu Lee, “Deeply-recursive convolutional network for image super-resolution,” in CVPR, 2016.

* ZSSR

​	A. Shocher, N. Cohen, and M. Irani, “zero-shot super-resolution using deep internal learning,” in CVPR, 2018

#### Post-upsampling SR

​	C. Dong, C. C. Loy, and X. Tang, “Accelerating the super- resolution convolutional neural network,” in ECCV, 2016.

​	W. Shi, J. Caballero, F. Huszar, J. Totz, A. P. Aitken, R. Bishop, ´D. Rueckert, and Z. Wang, “Real-time single image and video super-resolution using an efficient sub-pixel convolutional neural network,” in CVPR, 2016.

​	C. Ledig, L. Theis, F. Huszar, J. Caballero, A. Cunningham, ´ A. Acosta, A. P. Aitken, A. Tejani, J. Totz, Z. Wang et al., “Photo-realistic single image super-resolution using a generative adver-sarial network,” in CVPR, 2017.
​	B. Lim, S. Son, H. Kim, S. Nah, and K. M. Lee, “Enhanced deep residual networks for single image super-resolution,CVPRW,2017.
​	T. Tong, G. Li, X. Liu, and Q. Gao, “Image super-resolution using dense skip connections,” in ICCV, 2017

​	W. Han, S. Chang, D. Liu, M. Yu, M. Witbrock, and T. S. Huang, “Image super-resolution via dual-state recurrent networks,”in CVPR, 2018



#### Progressive Upsampling SR

​	W.-S. Lai, J.-B. Huang, N. Ahuja, and M.-H. Yang, “Deep laplacian pyramid networks for fast and accurate superresolution, in CVPR, 2017.
​	W.-S. Lai, J.-B. Huang, N. Ahuja, and M.-H. Yang, “Fast and accurate image super-resolution with deep laplacian pyramid networks,” TPAMI, 2018.
​	Y. Wang, F. Perazzi, B. McWilliams, A. Sorkine-Hornung, O. Sorkine-Hornung, and C. Schroers, “A fully progressive approach to single-image super-resolution,” in CVPRW, 2018.



#### Iterative Up-and-Down Sampling SR
​	R. Timofte, R. Rothe, and L. Van Gool, “Seven ways to improve example-based single image super resolution,” in CVPR,2016
​	W. Dong, L. Zhang, G. Shi, and X. Wu, “Nonlocal back projection for adaptive image enlargement,” in ICIP, 2009.

* DBPN

​	M. Haris, G. Shakhnarovich, and N. Ukita, “Deep backp-rojection networks for super-resolution,” in CVPR, 2018.

* SRFBN

​	 "Feedback Network for Image Super-Resolution，" in CVPR,2019. 


## 非监督学习



