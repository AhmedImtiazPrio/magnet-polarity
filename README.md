# Polarity Sampling: Quality and Diversity Control of Pre-Trained Generative Networks via Singular Values, CVPR 2022 (Oral)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://bit.ly/polarity-demo-colab)
### [Paper Link](https://arxiv.org/abs/2203.01993) | [Video Link](https://www.youtube.com/watch?v=zRKyx_dF89M)
[![polarity_sweep](https://user-images.githubusercontent.com/32792313/180766849-7e927dc2-cb0d-41f6-b614-aecc4b120ad4.gif)](#)


*Authors:* Ahmed Imtiaz Humayun, Randall Balestriero, Richard Baraniuk

*Abstract:* We present Polarity Sampling, a theoretically justified plug-and-play method for controlling the generation quality and diversity of pre-trained deep generative networks DGNs). Leveraging the fact that DGNs are, or can be approximated by, continuous piecewise affine splines, we derive the analytical DGN output space distribution as a function of the product of the DGN's Jacobian singular values raised to a power ρ. We dub ρ the polarity parameter and prove that ρ focuses the DGN sampling on the modes (ρ<0) or anti-modes (ρ>0) of the DGN output-space distribution. We demonstrate that nonzero polarity values achieve a better precision-recall (quality-diversity) Pareto frontier than standard methods, such as truncation, for a number of state-of-the-art DGNs. We also present quantitative and qualitative results on the improvement of overall generation quality (e.g., in terms of the Frechet Inception Distance) for a number of state-of-the-art DGNs, including StyleGAN3, BigGAN-deep, NVAE, for different conditional and unconditional image generation tasks. In particular, Polarity Sampling redefines the state-of-the-art for StyleGAN2 on the FFHQ Dataset to FID 2.57, StyleGAN2 on the LSUN Car Dataset to FID 2.27 and StyleGAN3 on the AFHQv2 Dataset to FID 3.95. Demo: [bit.ly/polarity-samp](http://bit.ly/polarity-samp)


#### Check out the codes for our previous paper, _MaGNET: Uniform Sampling from Deep Generative Network Manifolds Without Retraining_, ICLR 2022 at https://github.com/AhmedImtiazPrio/MaGNET
