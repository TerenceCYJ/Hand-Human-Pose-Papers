# Notes of Human Pose Estimation

## Table of Contents
 - [arXiv Papers](#arxiv-papers)
 - [Journal Papers](#journal-papers)
 - [Conference Papers](#conference-papers)
   - 2019: [CVPR](#2019-cvpr), [Others](#2019-others)
   - 2018: [CVPR](#2018-cvpr), [ECCV](#2018-eccv), [Others](#2018-others)
   - 2017: [CVPR](#2017-cvpr), [ICCV](#2017-iccv), [Others](#2017-others)
   - [Before 2016](#before-2016)
 - [Theses](#theses)
 - [Other Related Papers](#other-related-papers)
 - [Datasets](#datasets)
 - [Popular implementations](#popular-implementations)
   - [PyTorch](#pytorch)
   - [TensorFlow](#tensorflow)
   - [Torch](#torch)
   - [Others](#others)
 
 ## Basics
- [Human Pose Estimation 101](https://github.com/cbsudux/Human-Pose-Estimation-101)
- [awesome-human-pose-estimation](https://github.com/cbsudux/awesome-human-pose-estimation)
## arXiv Papers
##### [\[arXiv:1901.06792\]](https://arxiv.org/abs/1901.06792) Semantic Image Networks for Human Action Recognition. [\[PDF\]](https://arxiv.org/pdf/1901.06792.pdf)
_Sunder Ali Khowaja, Seok-Lyong Lee_
##### [\[arXiv:1812.10550\]](https://arxiv.org/abs/1812.10550) Learning to Recognize 3D Human Action from A New Skeleton-based Representation Using Deep Convolutional Neural Networks. [\[PDF\]](https://arxiv.org/pdf/1812.10550.pdf)
_Huy-Hieu Pham, Louahdi Khoudour, Alain Crouzil, Pablo Zegers, Sergio A. Velastin_
##### [\[arXiv:1807.02131\]](https://arxiv.org/abs/1807.02131) 3D Human Action Recognition with Siamese-LSTM Based Deep Metric Learning. [\[PDF\]](https://arxiv.org/pdf/1807.02131.pdf)
_Seyma Yucer, Yusuf Sinan Akgul_
##### [\[arXiv:1806.11230\]](https://arxiv.org/abs/1806.11230) Human Action Recognition and Prediction: A Survey. [\[PDF\]](https://arxiv.org/pdf/1806.11230.pdf)
_Yu Kong, Yun Fu_

## Journal Papers

## Conference Papers
### 2019 CVPR
##### Deep High-Resolution Representation Learning for Human Pose Estimation. [\[PDF\]](https://arxiv.org/pdf/1902.09212.pdf) [\[Code\]](https://github.com/leoxiaobin/deep-high-resolution-net.pytorch)
_Ke Sun, Bin Xiao, Dong Liu, [Jingdong Wang](https://jingdongwang2017.github.io/index.html)_
##### 3D human pose estimation in video with temporal convolutions and semi-supervised training. [\[Project Cite\]](https://dariopavllo.github.io/VideoPose3D/) [\[PDF\]](https://arxiv.org/pdf/1811.11742.pdf) [\[Code\]](https://github.com/facebookresearch/VideoPose3D)
_Dario Pavllo, Christoph Feichtenhofer, David Grangier, Michael Auli_
##### Learning Regularity in Skeleton Trajectories for Anomaly Detection in Videos. [\[PDF\]](https://arxiv.org/pdf/1903.03295.pdf)
_Romero Morais, Vuong Le, Truyen Tran, Budhaditya Saha, Moussa Mansour, Svetha Venkatesh_
##### PoseFix: Model-agnostic General Human Pose Refinement Network. [\[PDF\]](https://arxiv.org/pdf/1812.03595.pdf) [\[Code\]](https://github.com/mks0601/PoseFix_RELEASE)
_Gyeongsik Moon, Ju Yong Chang, Kyoung Mu Lee_
##### Dense Intrinsic Appearance Flow for Human Pose Transfer. [\[PDF\]](https://arxiv.org/pdf/1903.11326.pdf) [\[Code\]](http://mmlab.ie.cuhk.edu.hk/projects/pose-transfer/)
_Yining Li, Chen Huang, Chen Change Loy_
##### Putting Humans in a Scene: Learning Affordance in 3D Indoor Environments. [\[Project Cite\]](https://sites.google.com/view/3d-affordance-cvpr19) [\[PDF\]](https://arxiv.org/pdf/1903.05690.pdf)
_Xueting Li, Sifei Liu, Kihwan Kim, Xiaolong Wang, Ming-Hsuan Yang, Jan Kautz_
##### Learning 3D Human Dynamics from Video. [\[Project Cite\]](https://akanazawa.github.io/human_dynamics/) [\[PDF\]](https://arxiv.org/pdf/1812.01601.pdf)
_Angjoo Kanazawa, Jason Y. Zhang, Panna Felsen, Jitendra Malik_
##### RepNet: Weakly Supervised Training of an Adversarial Reprojection Network for 3D Human Pose Estimation. [\[PDF\]](https://arxiv.org/pdf/1902.09868.pdf)
_Bastian Wandt, Bodo Rosenhahn_
##### Self-Supervised Learning of 3D Human Pose using Multi-view Geometry. [\[PDF\]](https://arxiv.org/pdf/1903.02330.pdf) [\[Code\]](https://github.com/mkocabas/EpipolarPose)
_Muhammed Kocabas, Salih Karagoz, Emre Akbas_
##### Fast and Robust Multi-Person 3D Pose Estimation from Multiple Views. [\[Project Cite\]](https://zju3dv.github.io/mvpose/) [\[PDF\]](https://arxiv.org/pdf/1901.04111.pdf) [\[Code\]](https://github.com/zju3dv/mvpose)
_Junting Dong, Wen Jiang, Qixing Huang, Hujun Bao, Xiaowei Zhou_
##### PifPaf: Composite Fields for Human Pose Estimation. [\[PDF\]](https://arxiv.org/pdf/1903.06593.pdf) [\[Code\]]()
_Sven Kreiss, Lorenzo Bertoni, Alexandre Alahi_
##### Weakly-Supervised Discovery of Geometry-Aware Representation for 3D Human Pose Estimation. [\[PDF\]](https://arxiv.org/pdf/1903.08839.pdf) [\[Code\]]() *(Oral)*
_Xipeng Chen, Kwan-Yee Lin, Wentao Liu, Chen Qian, Xiaogang Wang, Liang Lin_
##### CrowdPose: Efficient Crowded Scenes Pose Estimation and A New Benchmark. [\[PDF\]](https://arxiv.org/pdf/1812.00324.pdf) [\[Code\]](https://github.com/Jeff-sjtu/CrowdPose)
_Jiefeng Li, Can Wang, Hao Zhu, Yihuan Mao, Hao-Shu Fang, Cewu Lu_

### 2019 Others
##### \[2019 WACV\]Unsupervised Feature Learning of Human Actions as Trajectories in Pose Embedding Manifold. [\[PDF\]](https://arxiv.org/pdf/1812.02592.pdf)
_Jogendra Nath Kundu, Maharshi Gor, Phani Krishna Uppala, R. Venkatesh Babu_

### 2018 ECCV

##### Simple Baselines for Human Pose Estimation and Tracking. [\[PDF\]](https://arxiv.org/pdf/1804.06208.pdf) [\[Code\]](https://github.com/Microsoft/human-pose-estimation.pytorch)
_Bin Xiao, Haiping Wu, Yichen Wei_

##### Skeleton-Based Action Recognition with Spatial Reasoning and Temporal Stack Learning. [\[PDF\]](http://172.16.24.181/openaccess.thecvf.com/content_ECCV_2018/papers/Chenyang_Si_Skeleton-Based_Action_Recognition_ECCV_2018_paper.pdf) 
_Chenyang Si, Ya Jing, Wei Wang, Liang Wang, Tieniu Tan_
##### Deformable Pose Traversal Convolution for 3D Action and Gesture Recognition. [\[PDF\]](http://172.16.24.186/openaccess.thecvf.com/content_ECCV_2018/papers/Junwu_Weng_Deformable_Pose_Traversal_ECCV_2018_paper.pdf) 
_Junwu Weng, Mengyuan Liu, Xudong Jiang, Junsong Yuan_
##### Learning Human-Object Interactions by Graph Parsing Neural Networks. [\[PDF\]](http://172.16.24.175/openaccess.thecvf.com/content_ECCV_2018/papers/Siyuan_Qi_Learning_Human-Object_Interactions_ECCV_2018_paper.pdf) 
_Siyuan Qi, Wenguan Wang, Baoxiong Jia, Jianbing Shen, Song-Chun Zhu_


### 2018 CVPR
##### End-to-end Recovery of Human Shape and Pose.  [\[Project Cite\]](https://akanazawa.github.io/hmr/) [\[PDF\]](https://arxiv.org/pdf/1712.06584.pdf) [\[Code\]](https://github.com/akanazawa/hmr)
_Angjoo Kanazawa, Michael J. Black, David W. Jacobs, Jitendra Malik_


### 2018 Others

### 2017 ICCV
##### Towards 3D Human Pose Estimation in the Wild: a Weakly-supervised Approach. [\[PDF\]](https://arxiv.org/abs/1704.02447) [\[Code\]](https://github.com/xingyizhou/pose-hg-3d)
_Xingyi Zhou, Qixing Huang, Xiao Sun, Xiangyang Xue, Yichen Wei_
### 2017 CVPR

## Theses

## Other Related Papers

## Datasets
### 2D
- [MPII Human Pose Dataset](http://human-pose.mpi-inf.mpg.de/)
- [LSP](http://sam.johnson.io/research/lsp.html)
- [FLIC](https://bensapp.github.io/flic-dataset.html)
- [FLIC-plus](https://cims.nyu.edu/~tompson/flic_plus.htm)

### 3D
- [Human3.6M](http://vision.imar.ro/human3.6m/description.php)
- [HumanEva](http://humaneva.is.tue.mpg.de/)
- [MPI-INF-3DHP](http://gvv.mpi-inf.mpg.de/3dhp-dataset/)
- [Unite The People](http://files.is.tuebingen.mpg.de/classner/up/)

## Popular implementations

### PyTorch
- [pytorch-pose-hg-3d](https://github.com/xingyizhou/Pytorch-pose-hg-3d)
- [3d_pose_baseline_pytorch](https://github.com/weigq/3d_pose_baseline_pytorch)
- [pytorch_Realtime_Multi-Person_Pose_Estimation](https://github.com/tensorboy/pytorch_Realtime_Multi-Person_Pose_Estimation)
- [AlphaPose](https://github.com/MVIG-SJTU/AlphaPose/tree/pytorch)
- [pytorch-pose](https://github.com/bearpaw/pytorch-pose)
- [human-pose-estimation.pytorch](https://github.com/Microsoft/human-pose-estimation.pytorch)

### TensorFlow
- [tf-pose-estimation](https://github.com/ildoonet/tf-pose-estimation)
- [pose-tensorflow](https://github.com/eldar/pose-tensorflow)

### Torch
- [pose-hg-train](https://github.com/umich-vl/pose-hg-train)
- [pose-hg-demo](https://github.com/umich-vl/pose-hg-demo)

### Others
- [openpose](https://github.com/CMU-Perceptual-Computing-Lab/openpose)
- [DensePose](https://github.com/facebookresearch/DensePose)
