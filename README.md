## Polarity Sampling: Quality and Diversity Control of Pre-Trained Generative Networks via Singular Values, CVPR 2022 (Oral)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://bit.ly/polarity-demo-colab)
### [Paper Link](https://arxiv.org/abs/2203.01993) | [Video Link](https://www.youtube.com/watch?v=zRKyx_dF89M)
<img src="https://github.com/AhmedImtiazPrio/magnet-polarity/blob/main/assets/polaritysweep.gif" height="250" alt_text="polarity_sweep_animation"/>

*Authors:* Ahmed Imtiaz Humayun, Randall Balestriero, Richard Baraniuk

*Abstract:* We present Polarity Sampling, a theoretically justified plug-and-play method for controlling the generation quality and diversity of pre-trained deep generative networks DGNs). Leveraging the fact that DGNs are, or can be approximated by, continuous piecewise affine splines, we derive the analytical DGN output space distribution as a function of the product of the DGN's Jacobian singular values raised to a power ρ. We dub ρ the polarity parameter and prove that ρ focuses the DGN sampling on the modes (ρ<0) or anti-modes (ρ>0) of the DGN output-space distribution. We demonstrate that nonzero polarity values achieve a better precision-recall (quality-diversity) Pareto frontier than standard methods, such as truncation, for a number of state-of-the-art DGNs. We also present quantitative and qualitative results on the improvement of overall generation quality (e.g., in terms of the Frechet Inception Distance) for a number of state-of-the-art DGNs, including StyleGAN3, BigGAN-deep, NVAE, for different conditional and unconditional image generation tasks. In particular, Polarity Sampling redefines the state-of-the-art for StyleGAN2 on the FFHQ Dataset to FID 2.57, StyleGAN2 on the LSUN Car Dataset to FID 2.27 and StyleGAN3 on the AFHQv2 Dataset to FID 3.95. Demo: [bit.ly/polarity-samp](http://bit.ly/polarity-samp)

<p float="left" align="center">
  <img src="https://user-images.githubusercontent.com/32792313/180782885-478ae2f3-e77d-4358-9b5f-a06804dca99d.gif"  height="250" alt_text="polarity_sweep_biggan"/>
  <img src="https://user-images.githubusercontent.com/32792313/180781556-1be1abb2-081a-4129-affa-8726e2a40f19.gif"  height="250" alt_text="polarity_sweep_biggan"/>
</p>

## Setup

Polarity Sampling is a Plug-and-Play method, we have separate google collabs for Tensorflow and Pytorch implementations of StyleGAN2 (TF), BigGAN-deep (TF), StyleGAN3 (Pytorch) and NVAE (Pytorch). The google collab code uses precomputed volume scalars to perform Polarity Sampling, therefore it requires only numpy and has no specific library dependencies. We also have submodules in this repo as examples for Tensorflow(=>1.15) and Pytorch(>=1.5), with methods that compute the volume scalars. We also provide the `MaGNET` helper library which allows training `tensorflow-gpu=>2` models and has polarity sampling modules built into it.

#### To use only the MaGNET library:

```shell
git clone https://github.com/AhmedImtiazPrio/magnet-polarity.git
```

#### To use submodules and compute volume scalars:

```shell
git clone --recurse-submodules https://github.com/AhmedImtiazPrio/magnet-polarity.git
```

or

```shell
git clone https://github.com/AhmedImtiazPrio/magnet-polarity.git
cd magnet-polarity
git submodule update --init --recursive
```

### Google Colabs

| Models | Dataset | Library | Links
| :---- | :---- | :---- | :----
| Stylegan2-ada | CIFAR10 | TF1.15 | 
| Stylegan2 | FFHQ | TF1.15 | 
| Stylegan3 | AFHQv2 | Pytorch1.10 | 
| BigGAN-deep | ImageNet | TF2.8 | 
| Guided Diffusion | ImageNet | &nbsp; | &nbsp;
| NVAE | MNIST | &nbsp; | &nbsp;




### Citation
```
@InProceedings{Humayun_2022_polarity,
    author    = {Humayun, Ahmed Imtiaz and Balestriero, Randall and Baraniuk, Richard},
    title     = {Polarity Sampling: Quality and Diversity Control of Pre-Trained Generative Networks via Singular Values},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month     = {June},
    year      = {2022},
    pages     = {10641-10650}
}

@InProceedings{Humayun_2022_magnet,
    author    = {Humayun, Ahmed Imtiaz and Balestriero, Randall and Baraniuk, Richard},
    title     = {MaGNET: Uniform Sampling from Deep Generative Network Manifolds Without Retraining},
    booktitle = {International Conference on Learning Representations (ICLR)},
    year      = {2022},
    url       = {https://openreview.net/forum?id=r5qumLiYwf9}
}
```


#### Check out the codes for _MaGNET: Uniform Sampling from Deep Generative Network Manifolds Without Retraining_, ICLR 2022 at https://github.com/AhmedImtiazPrio/MaGNET
