# SRCNN

【论文题目】

Image Super-Resolution Using Deep Convolutional Network.

【作者介绍】

**Chao Dong** 

* Beijing Institute of Technology,BS degree,2011

* University of Hongkong,PhD degree

* image super-resolution and denoising

**Chen Change Loy** 

*　Queen Mary University of London in 2010，PhD degree
*　Chinese University of Hong Kong

received the PhD degree in Computer Science from the Queen Mary University of London in 2010. He is currently a Research　AssistantProfessorintheDepartment of Information Engineering, Chinese University of Hong Kong. Previously he was a postdoctoral researcher at Vision Semantics Ltd. His research interests include computer vision and pattern recognition, with focus on face analysis, deep learning, and visual surveillance

**Kaiming He** 

＊　

received the BS degree from Tsinghua University in 2007, and the PhD degree from the Chinese University of Hong Kong in 2011. He is a researcher at Microsoft Research Asia (MSRA). He joined Microsoft Research Asia in 2011. His research interests include computer vision and computer graphics. He has won the Best Paper Award at the IEEE Conference on Computer Vision and Pattern Recognition (CVPR) 2009. He is a member of the IEEE.

**Xiaoou Tang** (S93-M96-SM02-F09) received the BS degree from the University of Science and Technology of China, Hefei, in 1990, the MS degree from the University of Rochester, New York,in1991,andthePhDdegreefromtheMassachusetts Institute of Technology, Cambridge, in 1996. He is a professor in the Department of Information Engineering and an associate dean (Research) of the Faculty of Engineering of the Chinese University of Hong Kong. He worked as the group manager of the Visual Computing Group at the Microsoft Research Asia, from 2005 to 2008. His research interests include computer vision, pattern recognition, and video processing. He received the Best Paper Award at the IEEE Conference on Computer Vision and Pattern Recognition (CVPR) 2009. He was a program chair of the IEEE International Conference on Computer Vision (ICCV) 2009 and he is an associate editor of the IEEE Transactions on Pattern Analysis and Machine Intelligence and the International Journal of Computer Vision. He is a fellow of the IEEE.

【解决的问题】

使用CNN直接学习低分辨率图像到高分辨率图像的非线性映射。替代传统方法学习LR dictionary—>HR dictionary 隐性学习的方式。

【研究内容】

1.提出了一种使用CNN超分的方法，该CNN可以直接学习LR map到HR map的非线性关系。

2.探索了基于样例学习（example learning）与传统稀疏编码（traditional sparse-coding-based SR）方法的关系。并基于此关系来设计神经网络。

3.证明了深度学习对超分问题的有效性，可以取得好的质量，并且加快速度。

【网络结构】

![network](pic\SRCNN\network.JPG)

* patch extraction and representation
* Non-linear mapping
* Reconstruction

【创新点】



【结论】



【我的思考】