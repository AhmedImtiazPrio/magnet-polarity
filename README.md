## Polarity Sampling: Quality and Diversity Control of Pre-Trained Generative Networks via Singular Values, CVPR 2022 (Oral)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://bit.ly/polarity-demo-colab)
### [Paper Link](https://arxiv.org/abs/2203.01993) | [Video Link](https://www.youtube.com/watch?v=zRKyx_dF89M)
<img src="https://github.com/AhmedImtiazPrio/magnet-polarity/blob/main/assets/polaritysweep.gif"  height="300" />


*Authors:* Ahmed Imtiaz Humayun, Randall Balestriero, Richard Baraniuk

*Abstract:* We present Polarity Sampling, a theoretically justified plug-and-play method for controlling the generation quality and diversity of pre-trained deep generative networks DGNs). Leveraging the fact that DGNs are, or can be approximated by, continuous piecewise affine splines, we derive the analytical DGN output space distribution as a function of the product of the DGN's Jacobian singular values raised to a power ρ. We dub ρ the polarity parameter and prove that ρ focuses the DGN sampling on the modes (ρ<0) or anti-modes (ρ>0) of the DGN output-space distribution. We demonstrate that nonzero polarity values achieve a better precision-recall (quality-diversity) Pareto frontier than standard methods, such as truncation, for a number of state-of-the-art DGNs. We also present quantitative and qualitative results on the improvement of overall generation quality (e.g., in terms of the Frechet Inception Distance) for a number of state-of-the-art DGNs, including StyleGAN3, BigGAN-deep, NVAE, for different conditional and unconditional image generation tasks. In particular, Polarity Sampling redefines the state-of-the-art for StyleGAN2 on the FFHQ Dataset to FID 2.57, StyleGAN2 on the LSUN Car Dataset to FID 2.27 and StyleGAN3 on the AFHQv2 Dataset to FID 3.95. Demo: [bit.ly/polarity-samp](http://bit.ly/polarity-samp)

### Citation
```
@InProceedings{Humayun_2022_CVPR,
    author    = {Humayun, Ahmed Imtiaz and Balestriero, Randall and Baraniuk, Richard},
    title     = {Polarity Sampling: Quality and Diversity Control of Pre-Trained Generative Networks via Singular Values},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month     = {June},
    year      = {2022},
    pages     = {10641-10650}
}
```


#### Check out the codes for our previous paper, _MaGNET: Uniform Sampling from Deep Generative Network Manifolds Without Retraining_, ICLR 2022 at https://github.com/AhmedImtiazPrio/MaGNET
