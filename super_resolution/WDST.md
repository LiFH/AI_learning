# WDST (wavelet domain style transform )

【整理时间】2019.11.27

【论文题目】Wavelet Domain Style Transfer for an Effiective Perception-distortion Tradoff in Single Image Super-Resolution

【作者介绍】Xin Deng,Ren Yang, Mai Xu, Pier Luigi Dragotti.

【发表会议】ICCV 2019

【解决问题】

SISR任务期待从一张地分辨率图像重建出高分辨率图像，同时保证精确性和真实性。近来GAN对低失真（low distortion）和高感知质量（high perceptual quality）很好的权衡。

本文提出了一种小波域风格转换（wavelet domain style transform）方法可以取得比GAN更好的权衡。固定的小波转换（stationary wavelet transform，SWT）可以将一张图像分解为高频（high-frequency）和低频（low-frequency）子波段。

低频子波段可以通过增强网络来提升目标（objective）质量，高频子波段可以提升感知（perceptual）质量。


【网络结构】

【总结】
此篇论文基于小波域转换下提出了一种很好的方法，解决了SISR任务中的感知失真（perception-distortion）冲突。

【我的思考】

将无监督和小波变换结合会不会产生更好的结果呢？

