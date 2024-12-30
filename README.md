# Inverse Rendering - A Comparative Survey

This is our survey on a longstanding Computer Vision and Computer Graphics problem: **Inverse Rendering**. This survey also is the product of our final project in the 2024F Computer Vision course (515619電腦視覺) taught by professor Wei-Chen Chiu (邱維辰) at National Yang Ming Chiao Tung University, Taiwan.

To our knowledge, the last published survey was done by [Patow et. al.](https://onlinelibrary.wiley.com/doi/abs/10.1111/j.1467-8659.2003.00716.x), dating back to 2003. Thus, there is a clear need for a modern review of this field. Furthermore,  Our study of computer vision fundamentals has revealed numerous recent advances - from differentiable rendering to neural radiance fields - that warrant systematic analysis. This motivates us to synthesize these developments and their applications in solving the inverse rendering problem.

We refer readers to the **PDF file** for the main work.

## NeRF-based Inverse Rendering

### 1. NeRV: Neural Reflectance and Visibility Fields for Relighting and View Synthesis

**Authors**: Pratul P. Srinivasan, Boyang Deng, Xiuming Zhang, Matthew Tancik, Ben Mildenhall, Jonathan T. Barron

**Publication**: CVPR 2021

**Note**: Assume known environment illumination. Normal estimation from density is from here.

[📄 Paper](https://arxiv.org/abs/2012.03927) | [🌐 Project Page](https://pratulsrinivasan.github.io/nerv/) | [💻 Code (not yet)]() 



### 2. NeRD: Neural Reflectance Decomposition from Image Collections

**Authors**: Mark Boss, Raphael Braun, Varun Jampani, Jonathan T. Barron, Ce Liu, Hendrik P.A. Lensch

**Publication**: ICCV 2021

[📄 Paper](https://arxiv.org/abs/2012.03918) | [🌐 Project Page](https://markboss.me/publication/2021-nerd/) | [💻 Code](https://github.com/cgtuebingen/NeRD-Neural-Reflectance-Decomposition) 



### 3. Neural Ray-Tracing: Learning Surfaces and Reflectance for Relighting and View Synthesis

**Authors**: Julian Knodt, Joe Bartusek, Seung-Hwan Baek, Felix Heide

**Publication**: Arxiv 2021

[📄 Paper](https://arxiv.org/abs/2104.13562) | [💻 Code](https://github.com/princeton-computational-imaging/neural_raytracing) 



### 4. NeRFactor: Neural Factorization of Shape and Reflectance Under an Unknown Illumination

**Authors**: Xiuming Zhang, Pratul P. Srinivasan, Boyang Deng, Paul Debevec, William T. Freeman, Jonathan T. Barron

**Publication**: SIGGRAPH Asia 2021

**Note**: It is undoubtedly an awesome piece of work. "Normal Smoothness" originates from this article. My only regret is that I think the authors were aware that the IR framework based on NeRF struggles to decouple shadows and materials, but they did not mention this in the Limitations section. Their scenarios of **reducing light intensity** (Not the same as vanilla NeRF scenes with obvious shadow and indirect illumination) still impacted many subsequent works that focused on novel view synthesis rather than the accuracy of material decoupling. This is very important for relighting to remove artifacts.

[📄 Paper](https://arxiv.org/pdf/2106.01970.pdf) | [🌐 Project Page](https://xiuming.info/projects/nerfactor/) | [💻 Code](https://github.com/google/nerfactor) 



### 5. Neural-PIL: Neural Pre-Integrated Lighting for Reflectance Decomposition

**Authors**: Mark Boss, Varun Jampani, Raphael Braun, Ce Liu, Jonathan T. Barron, Hendrik P.A. Lensch

**Publication**: NeurIPS 2021

[📄 Paper](https://arxiv.org/abs/2110.14373) | [🌐 Project Page](https://markboss.me/publication/2021-neural-pil/) | [💻 Code](https://github.com/cgtuebingen/Neural-PIL) 



### 6. PS-NeRF: Neural Inverse Rendering for Multi-view Photometric Stereo

**Authors**: Wenqi Yang, Guanying Chen, Chaofeng Chen, Zhenfang Chen, Kwan-Yee K. Wong

**Publication**: ECCV 2022

[📄 Paper](https://arxiv.org/abs/2207.11406) | [🌐 Project Page](https://ywq.github.io/psnerf/) | [💻 Code](https://github.com/ywq/psnerf) 



### 7. NeILF: Neural Incident Light Field for Physically-based Material Estimation

**Authors**: Yao Yao, Jingyang Zhang, Jingbo Liu, Yihang Qu, Tian Fang, David McKinnon, Yanghai Tsin, Long Quan

**Publication**: ECCV 2022

[📄 Paper](https://arxiv.org/abs/2203.07182) | [💻 Code](https://github.com/apple/ml-neilf) 



### 8. L-Tracing: Fast Light Visibility Estimation on Neural Surfaces by Sphere Tracing

**Authors**: Ziyu Chen, Chenjing Ding, Jianfei Guo, Dongliang Wang, Yikang Li, Xuan Xiao, Wei Wu, Li Song

**Publication**: ECCV 2022

**Note**: Visibility estimation without training.

[📄 Paper](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136750214.pdf) | [💻 Code](https://github.com/ziyc/L-Tracing) 



### 9. SAMURAI: Shape And Material from Unconstrained Real-world Arbitrary Image collections

**Authors**: Mark Boss, Andreas Engelhardt, Abhishek Kar, Yuanzhen Li, Deqing Sun, Jonathan T. Barron, Hendrik P. A. Lensch, Varun Jampani

**Publication**: NeurIPS 2022

[📄 Paper](https://arxiv.org/abs/2205.15768) | [🌐 Project Page](https://markboss.me/publication/2022-samurai/) | [💻 Code](https://github.com/google/samurai) 



### 10. Flash Cache: Reducing Bias in Radiance Cache Based Inverse Rendering

**Authors**: Benjamin Attal, Dor Verbin, Ben Mildenhall, Peter Hedman, Jonathan T. Barron, Matthew O'Toole, Pratul P. Srinivasan

**Publication**: ECCV 2024 (Oral)

[📄 Paper](https://www.arxiv.org/abs/2409.05867) | [🌐 Project Page](https://benattal.github.io/flash-cache/) | [💻 Code]()

<br>

## 3DGS-based Inverse Rendering

### 1. Relightable 3D Gaussian: Real-time Point Cloud Relighting with BRDF Decomposition and Ray Tracing

**Authors**: Jian Gao, Chun Gu, Youtian Lin, Hao Zhu, Xun Cao, Li Zhang, Yao Yao

**Publication**: ECCV 2024

[📄 Paper](https://arxiv.org/abs/2311.16043) | [🌐 Project Page](https://nju-3dv.github.io/projects/Relightable3DGaussian/) | [💻 Code](https://github.com/NJU-3DV/Relightable3DGaussian) 

### 2. GaussianShader: 3D Gaussian Splatting with Shading Functions for Reflective Surfaces

**Authors**: Yingwenqi Jiang, Jiadong Tu, Yuan Liu, Xifeng Gao, Xiaoxiao Long, Wenping Wang, Yuexin Ma

**Publication**: CVPR 2024

[📄 Paper](https://arxiv.org/abs/2311.17977) | [🌐 Project Page](https://asparagus15.github.io/GaussianShader.github.io/) | [💻 Code](https://github.com/Asparagus15/GaussianShader)

### 3. GS-IR: 3D Gaussian Splatting for Inverse Rendering

**Authors**: Zhihao Liang, Qi Zhang, Ying Feng, Ying Shan, Kui Jia

**Publication**: CVPR 2024

[📄 Paper](https://arxiv.org/abs/2311.16473) | [🌐 Project Page](https://lzhnb.github.io/project-pages/gs-ir.html) | [💻 Code](https://github.com/lzhnb/GS-IR)

### 4. GIR: 3D Gaussian Inverse Rendering for Relightable Scene Factorization

**Authors**:  Yahao Shi, Yanmin Wu, Chenming Wu, Xing Liu, Chen Zhao, Haocheng Feng, Jingtuo Liu, Liangjun Zhang, Jian Zhang, Bin Zhou, Errui Ding, Jingdong Wang

**Publication**: Arxiv 2023

[📄 Paper](https://arxiv.org/abs/2312.05133) | [🌐 Project Page](https://3dgir.github.io/) | [💻 Code (Not yet)]()

### 5. DeferredGS: Decoupled and Editable Gaussian Splatting with Deferred Shading

**Authors**:  Tong Wu, Jia-Mu Sun, Yu-Kun Lai, Yuewen Ma, Leif Kobbelt, Lin Gao

**Publication**: Arxiv 2024

[📄 Paper](https://arxiv.org/abs/2404.09412) 

### 6. Differentiable Point-based Inverse Rendering

**Authors**: Hoon-Gyu Chung, Seokjun Choi, Seung-Hwan Baek

**Publication**: CVPR 2024

[📄 Paper](https://arxiv.org/abs/2312.02480) | [🌐 Project Page](https://hg-chung.github.io/DPIR/) | [💻 Code](https://github.com/hg-chung/DPIR)

### 7. GS-ROR: 3D Gaussian Splatting for Reflective Object Relighting via SDF Priors

**Authors**: Zuoliang Zhu, Beibei Wang, Jian Yang

**Publication**: Arxiv 2024

[📄 Paper](https://arxiv.org/pdf/2406.18544)

### 8. PRTGS: Precomputed Radiance Transfer of Gaussian Splats for Real-Time High-Quality Relighting

**Authors**: Yijia Guo, Yuanxi Bai, Liwen Hu, Ziyi Guo, Mianzhi Liu, Yu Cai, Tiejun Huang, Lei Ma

**Publication**: Arxiv 2024

[📄 Paper](https://www.arxiv.org/abs/2408.03538)

### 9. Progressive Radiance Distillation for Inverse Rendering with Gaussian Splatting

**Authors**: Keyang Ye, Qiming Hou, Kun Zhou

**Publication**: Arxiv 2024

[📄 Paper](https://arxiv.org/abs/2408.07595)

### 10. Subsurface Scattering for 3D Gaussian Splatting

**Authors**: Jan-Niklas Dihlmann, Arjun Majumdar, Andreas Engelhardt, Raphael Braun, Hendrik P.A. Lensch

**Publication**: Arxiv 2024

[📄 Paper](https://www.arxiv.org/abs/2408.12282) | [🌐 Project Page](https://sss.jdihlmann.com/) | [💻 Code](https://github.com/cgtuebingen/SSS-GS)

### 11. Efficient Relighting with Triple Gaussian Splatting

**Authors**: Zoubin Bi, Yixin Zeng, Chong Zeng, Fan Pei, Xiang Feng, Kun Zhou, Hongzhi Wu

**Publication**: SIGGRAPH ASIA 2024

[📄 Paper](https://gsrelight.github.io/pdfs/GS3.pdf) | [🌐 Project Page](https://gsrelight.github.io/) | [💻 Code]()


### 12. GI-GS: Global Illumination Decomposition on Gaussian Splatting for Inverse Rendering

**Authors**: Hongze Chen, Zehong Lin, Jun Zhang

**Publication**: arXiv 2410.02619

[📄 Paper](https://arxiv.org/pdf/2410.02619) | [🌐 Project Page](https://stopaimme.github.io/GI-GS/) | [💻 Code](https://github.com/stopaimme/GI-GS-official-implementation)

### 13. GlossyGS: Inverse Rendering of Glossy Objects with 3D Gaussian Splatting

**Authors**: Shuichang Lai, Letian Huang, Jie Guo, Kai Cheng, Bowen Pan, Xiaoxiao Long, Jiangjing Lyu, Chengfei Lv, Yanwen Guo

**Publication**: ArXiv 2024

[📄 Paper](https://arxiv.org/abs/2410.13349)

### 14. GeoSplatting: Towards Geometry Guided Gaussian Splatting for Physically-based Inverse Rendering

**Author**: Kai Ye, Chong Gao, Guanbin Li, Wenzheng Chen, Baoquan Chen

**Publication**: Arxiv 2024

[📄 Paper](https://arxiv.org/abs/2410.24204) | [🌐 Project Page](https://pku-vcl-geometry.github.io/GeoSplatting/) | [💻 Code](https://github.com/PKU-VCL-Geometry/geosplatting)

### 15. IRGS: Inter-Reflective Gaussian Splatting with 2D Gaussian Ray Tracing

**Author**: Chun Gu, Xiaofei Wei, Zixuan Zeng, Yuxuan Yao, Li Zhang

**Publication**: Arxiv 2024

[📄 Paper](https://arxiv.org/abs/2412.15867) | [🌐 Project Page](https://fudan-zvg.github.io/IRGS/) | [💻 Code](https://github.com/fudan-zvg/IRGS)

## Inverse Rendering with Diffusion Prior

### 1. Diffusion Posterior Illumination for Ambiguity-aware Inverse Rendering (DPI)

**Authors**: Linjie Lyu, Ayush Tewari, Marc Habermann, Shunsuke Saito, Michael Zollhöfer, Thomas Leimkühler, Christian Theobalt

**Publication**: SIGGRAPH Asia 2023

[📄 Paper](https://arxiv.org/abs/2310.00362) | [🌐 Project Page](https://vcai.mpi-inf.mpg.de/projects/2023-DPE/) | [💻 Code](https://github.com/LinjieLyu/DPI)

### 2. Diffusion Reflectance Map: Single-Image Stochastic Inverse Rendering of Illumination and Reflectance

**Authors**: Yuto Enyo, Ko Nishino

**Publication**: CVPR 2024 Highlight

[📄 Paper](https://arxiv.org/abs/2312.04529) | [🌐 Project Page](https://vision.ist.i.kyoto-u.ac.jp/research/drm/) | [💻 Code](https://github.com/kyotovision-public/DRMNet)

### 3. IntrinsicAnything: Learning Diffusion Priors for Inverse Rendering Under Unknown Illumination

**Authors**: Xi Chen, Sida Peng, Dongchen Yang, Yuan Liu, Bowen Pan, Chengfei Lv, Xiaowei Zhou

**Publication**: ECCV 2024

[📄 Paper](https://arxiv.org/abs/2404.11593) | [🌐 Project Page](https://zju3dv.github.io/IntrinsicAnything/) | [💻 Code](https://github.com/zju3dv/IntrinsicAnything)


### 4. MaterialFusion: Enhancing Inverse Rendering with Material Diffusion Priors

**Authors**: Yehonathan Litman, Or Patashnik, Kangle Deng, Aviral Agrawal, Rushikesh Zawar, Fernando De la Torre, Shubham Tulsiani

**Publication**: Arxiv 2024

[📄 Paper](https://arxiv.org/abs/2409.15273) | [🌐 Project Page](https://yehonathanlitman.github.io/material_fusion/) | [💻 Code](https://github.com/yehonathanlitman/MaterialFusion)


