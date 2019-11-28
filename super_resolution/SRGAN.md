# SRGAN

【论文题目】Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network

【作者】 Christian Ledig，Lucas Theis...    (Twitter)

【会议】ECCV 2017

【解决问题】

MSE loss是一种像素级（Pixel-wise）的损失函数，在最小化MSE loss时容易丢失如纹理的高频信息，最后的结果也是过于平滑的，并且感知（perceptual）质量往往一般。

那么在超分时，更大的放大因子（4x）如何恢复更好的纹理细节？

针对此问题，作者提出了一种由对抗损失（adversarial loss）和内容损失（content loss）组成的感知损失（perceptual loss）。

$$ l^{SR} = l_X^{SR} + 10^{-3}l_{Gen}^{SR} $$

其中 $ l_X^{SR}$为内容（content）损失，$l_{Gen}^{SR}$为感知损失。





【总结】



【我的思考】



