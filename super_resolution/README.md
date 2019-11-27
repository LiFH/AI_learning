# super resolution
超分辨率问题一直是一个很热门的研究领域，近来随着深度学习的发展，single image super resolution（SISR）也得到迅速的发展。

超分辨率按照是否有匹配的patch可以分为监督学习和非监督学习。



以下为超分论文目录(持续更新中，以后每天至少更新一篇)

## 1.监督学习

### 1.1 upsampling

按照上采样（upsampling）的位置可以将超分网络分为四大类：Pre-upsampling SR、Post-upsampling、Progressive Upsampling SR、Iterative Up-and-Down Sampling SR

#### Pre-upsampling SR

| model             | paper with link                                              | author                                 | conference | code                                         |
| ----------------- | ------------------------------------------------------------ | -------------------------------------- | ---------- | -------------------------------------------- |
| [SRCNN](SRCNN.md) | [Learning a deep convolutional network for image super-resolution](http://mmlab.ie.cuhk.edu.hk/projects/SRCNN.html) | C. Dong, C. C. Loy, K. He, and X. Tang | ECCV,2014. |                                              |
| DRCN              | Deeply-recursive convolutional network for image super-resolution | J. Kim, J. Kwon Lee, and K. Mu Lee     | CVPR,2016. |                                              |
| Memnet            | Memnet: A persistent memory network for image restoration    | Y. Tai, J. Yang, X. Liu, and C. Xu     | ICCV,2017. |                                              |
| DRRN              | Image super-resolution via deep recursive residual network   | Y. Tai, J. Yang, and X. Liu            | CVPR,2017. |                                              |
| [ZSSR](ZSSR.md)   | [zero-shot super-resolution using deep internal learning](http://www.wisdom.weizmann.ac.il/~vision/zssr/) | A. Shocher, N. Cohen, and M. Irani     | CVPR,2018. | [code](https://github.com/assafshocher/ZSSR) |

#### Post-upsampling SR

| model      | paper with link                                              | author                                                       | conference  | code |
| ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------- | :--- |
| FSRCNN     | Accelerating the super- resolution convolutional neural network | C. Dong, C. C. Loy, and X. Tang                              | ECCV,2016.  |      |
| ESPCN      | Real-time single image and video super-resolution using an efficient sub-pixel convolutional neural network | W. Shi, J. Caballero, F. Huszar, J. Totz, A. P. Aitken, R. Bishop, ´D. Rueckert, and Z. Wang | CVPR,2016.  |      |
| SRGAN      | Photo-realistic single image super-resolution using a generative adver-sarial network | C. Ledig, L. Theis, F. Huszar, J. Caballero, A. Cunningham, ´ A. Acosta, A. P. Aitken, A. Tejani, J. Totz, Z. Wang et al. | CVPR,2017.  |      |
| EDSR       | Enhanced deep residual networks for single image super-resolution | B. Lim, S. Son, H. Kim, S. Nah, and K. M. Lee                | CVPRW,2017. |      |
| SRDenseNet | Image super-resolution using dense skip connections          | T. Tong, G. Li, X. Liu, and Q. Gao                           | ICCV,2017.  |      |
| DSRN       | Image super-resolution via dual-state recurrent networks     | W. Han, S. Chang, D. Liu, M. Yu, M. Witbrock, and T. S. Huang | CVPR,2018.  |      |

#### Progressive Upsampling SR

| model     | paper with link                                              | author                                                       | conference  | code |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------- | ---- |
| LapSRN    | Deep laplacian pyramid networks for fast and accurate super resolution | W.-S. Lai, J.-B. Huang, N. Ahuja, and M.-H. Yang             | CVPR,2017.  |      |
| MS-LapSRN | Fast and accurate image super-resolution with deep laplacian pyramid networks | W.-S. Lai, J.-B. Huang, N. Ahuja, and M.-H. Yang             | TPAMI,2018. |      |
| ProSR     | A fully progressive approach to single-image super-resolution | Y. Wang, F. Perazzi, B. McWilliams, A. Sorkine-Hornung, O. Sorkine-Hornung, and C. Schroers | CVPRW,2018. |      |

#### Iterative Up-and-Down Sampling SR

feedback network

| model | paper with link                                    | author                                   | conference | code |
| ----- | -------------------------------------------------- | ---------------------------------------- | ---------- | ---- |
| DBPN  | Deep backp-rojection networks for super-resolution | M. Haris, G. Shakhnarovich, and N. Ukita | CVPR,2018. |      |
| SRFBN | Feedback Network for Image Super-Resolution        |                                          | CVPR,2019. |      |

### 1.2 Network Design

#### Residual Learning
##### Global Residual Learning

| model  | paper with link                                              | author                             | conference | code |
| ------ | ------------------------------------------------------------ | ---------------------------------- | ---------- | ---- |
| VDSR   | Accurate image super resolution using very deep convolutional networks | J. Kim, J. Kwon Lee, and K. Mu Lee | CVPR,2016. |      |
| Memnet | Memnet: A persistent memory network for image restoration    | Y. Tai, J. Yang, X. Liu, and C. Xu | ICCV,2017. |      |
| DRRN   | Image super-resolution via deep recursive residual network   | Y. Tai, J. Yang, and X. Liu        | CVPR,2017. |      |
| IDN    | Fast and accurate single image super-resolution via information distillation network | Z. Hui, X. Wang, and X. Gao        | CVPR,2018. |      |

##### Local Residual Learning

| model   | paper with link                                              | author                                                       | conference  | code |
| ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------- | ---- |
| RED-Net | Image restoration using very deep convolutional encoder-decoder networks with symmetric skip connections | X. Mao, C. Shen, and Y.-B. Yang                              | NIPS,2016.  |      |
| RCAN    | Image super-resolution using very deep residual channel attention networks | Y. Zhang, K. Li, K. Li, L. Wang, B. Zhong, and Y. Fu         | ECCV,2018.  |      |
| DSRN    | Image super-resolution via dual-state recurrent networks     | W. Han, S. Chang, D. Liu, M. Yu, M. Witbrock, and T. S. Huang | CVPR,2018.  |      |
| MSRN    | Multi-scale residual network for image super-resolution      | J. Li, F. Fang, K. Mei, and G. Zhang                         | ECCV, 2018. |      |



#### Recursive Learning

​	to achieve large receptive field and learn higher-level features 

| model  | paper with link                                              | author                             | conference | code |
| ------ | ------------------------------------------------------------ | ---------------------------------- | ---------- | ---- |
| DRCN   | Deeply-recursive convolutional network for image super-resolution | J. Kim, J. Kwon Lee, and K. Mu Lee | CVPR,2016. |      |
| DRRN   | Image super-resolution via deep recursive residual network   | Y. Tai, J. Yang, and X. Liu        | CVPR,2017. |      |
| MemNet | Memnet: A persistent memory network for image restoration    | Y. Tai, J. Yang, X. Liu, and C. Xu | ICCV,2017. |      |
| CARN   | Fast, accurate, and lightweight super-resolution with cascading residual network | N. Ahn, B. Kang, and K.-A. Sohn    | ECCV,2018. |      |
|        | Embedded Block Residual Network: A Recursive Restoration Model for Single-Image Super-Resolution | Yajun Qiu,Ruxin Wang,Dapeng Tao    | ICCV,2019  |      |



#### Multi-path Learning
##### Global Mutil-path Learning

| model                            | paper with link                                              | author                                                   | conference  | code |
| -------------------------------- | ------------------------------------------------------------ | -------------------------------------------------------- | ----------- | ---- |
| LapSRN                           | Deep laplacian pyramid networks for fast and accurate super resolution | W.-S. Lai, J.-B. Huang, N. Ahuja, and M.-H. Yang         | CVPR,2017.  |      |
| DSRN                             | W. Han, S. Chang, D. Liu, M. Yu, M. Witbrock, and T. S. Huang | Image super-resolution via dual-state recurrent networks | CVPR,2018.  |      |
| Pixel recursive super resolution | Pixel recursive super resolution                             | R. Dahl, M. Norouzi, and J. Shlens                       | ICCV, 2017. |      |
| CNF(context-wise network fusion) | Image super resolution based on fusing multiple convolution neural networks | H. Ren, M. El-Khamy, and J. Lee                          | CVPRW,2017. |      |

##### Local Mutil-path Learning

| model     | paper with link                                              | author                                        | conference  | code |
| --------- | ------------------------------------------------------------ | --------------------------------------------- | ----------- | ---- |
| EDSR MDSR | Enhanced deep residual networks for single image super resolution | B. Lim, S. Son, H. Kim, S. Nah, and K. M. Lee | CVPRW,2017. |      |
| MSRN      | Multi-scale residual network for image super-resolution      | J.Li,F.Fang,K.Mei,andG.Zhang                  | ECCV, 2018. |      |

##### Scale-specific Multi-path Learning		

| model | paper with link                                              | author                                                       | conference  | code |
| ----- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------- | ---- |
|       | Fast,accurate,and light weight super-resolution with cascading residual network | N.Ahn,B.Kang,and K.-A.Sohn                                   | ECCV,2018.  |      |
|       | A fully progressive approach to single-image super-resolution | Y. Wang, F. Perazzi, B. McWilliams, A. Sorkine-Hornung, O. Sorkine-Hornung, and C. Schroers | CVPRW,2018. |      |

#### Dense Connections
​	

| model  | paper with link                                              | author                                                       | conference           | code |
| ------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------- | ---- |
|        | Densely connected convolutional networks                     | G. Huang, Z. Liu, L. Van Der Maaten, and K. Q. Weinberger    | CVPR,2017.           |      |
|        | Image super-resolution using dense skip connections          | T. Tong, G. Li, X. Liu, and Q. Gao                           | ICCV,2017.           |      |
| Memnet | Memnet: A persistent memory network for image restoration    | Y. Tai, J. Yang, X. Liu, and C. Xu                           | ICCV,2017.           |      |
|        | Fast,accurate,and light weight super-resolution with cascading residual network | N.Ahn,B.Kang,andK.-A.Sohn                                    | ECCV,2018.           |      |
|        | Residual dense network for image super-resolution            | Y. Zhang, Y. Tian, Y. Kong, B. Zhong, and Y. Fu              | CVPR,2018.           |      |
| ESRGAN | Esrgan: Enhanced super-resolution generative adversarial networks | X. Wang, K. Yu, S. Wu, J. Gu, Y. Liu, C. Dong, C. C. Loy, Y. Qiao, and X. Tang | ECCV Workshop, 2018. |      |
|        | Deep-back projection networks for super-resolution           | M.Haris,G.Shakhnarovich,andN.Ukita                           | CVPR, 2018.          |      |

#### Channel Attention

| model | paper with link                                              | author                                               | conference | code |
| ----- | ------------------------------------------------------------ | ---------------------------------------------------- | ---------- | ---- |
|       | Image super-resolution using very deep residual channel attention networks | Y. Zhang, K. Li, K. Li, L. Wang, B. Zhong, and Y. Fu | ECCV,2018. |      |
|       | Squeeze-and-excitation networks                              | J. Hu, L. Shen, and G. Sun                           | CVPR,2018. |      |

#### Pyramid Pooling

| model | paper with link                                              | author                              | conference | code |
| ----- | ------------------------------------------------------------ | ----------------------------------- | ---------- | ---- |
|       | Spatial pyramid pooling in deep convolutional networks for visual recognition | K. He, X. Zhang, S. Ren, and J. Sun | ECCV, 2014 |      |
|       | Pyramid scene parsing network                                | H.Zhao,J.Shi,X.Qi,X.Wang,andJ.Jia   | CVPR,2017. |      |
|       |                                                              |                                     |            |      |

#### Wavelet Transformation（小波变换）

| model           | paper with link                                              | author                                         | conference  | code |
| --------------- | ------------------------------------------------------------ | ---------------------------------------------- | ----------- | ---- |
|                 | Beyond deep residual learning for image restoration: Persistent homology-guided manifold simplification | W. Bae, J. J. Yoo, and J. C. Ye                | CVPRW,2017. |      |
| DWSR            | Deep wavelet prediction for image super-resolution           | T. Guo, H. S. Mousavi, T. H. Vu, and V. Monga  | CVPRW,2017. |      |
|                 | Wavelet-srnet: A wavelet-based cnn for multi-scale face super resolution | H. Huang, R. He, Z. Sun, T. Tan et al.         | ICCV, 2017. |      |
|                 | Multi-level wavelet-cnn for image restoration                | P. Liu, H. Zhang, K. Zhang, L. Lin, and W. Zuo | CVPRW,2018. |      |
| [WDST](WDST.md) | Wavelet Domain Style Transfer for an Effective Perception-distortion Tradeoff in Single Image Super-Resolution | Xin Deng,Ren Yang,Mai Xu,Pier Luigi Dragotti   | ICCV,2019   |      |

#### blind sr

| model | paper with link | author | conference | code |
| ----- | --------------- | ------ | ---------- | ---- |
| SRMD  |                 |        |            |      |
|       |                 |        |            |      |
|       |                 |        |            |      |


## 2.非监督学习

| model           | paper with link                                              | author                                                   | conference  | code |
| --------------- | ------------------------------------------------------------ | -------------------------------------------------------- | ----------- | ---- |
| [ZSSR](ZSSR.md) | zero-shot super-resolution using deep internal learning      | A. Shocher, N. Cohen, and M. Irani                       | CVPR, 2018. |      |
|                 | Unsupervised image super-resolution using cycle-in-cycle generative adversarial networks | Y. Yuan, S. Liu, J. Zhang, Y. Zhang, C. Dong, and L. Lin | CVPRW,2018. |      |
|                 | Deep image prior                                             | D. Ulyanov, A. Vedaldi, and V. Lempitsky                 | CVPR, 2018. |      |

## 3.弱监督学习

##### Weakly-supervised Super-Resolution

Learned Degradation

| model | paper with link                                              | author                                  | conference | code |
| ----- | ------------------------------------------------------------ | --------------------------------------- | ---------- | ---- |
|       | To learn image super resolution,use a gan to learn how to do image degradation ﬁrst | A. Bulat, J. Yang, and G. Tzimiropoulos | ECCV, 2018 |      |





