# 《SHPR-Net: Deep Semantic Hand Pose Regression From Point Clouds》
* Authors: XINGHAO CHEN, GUIJIN WANG, CAIRONG ZHANG, TAE-KYUN KIM, XIANGYANG JI, IEEE Access, 2018
* Keywords: Semantic Segmentation + Pose Regression
### Background:
- Mapping a 2D depth image to 3D joint coordinates is a highly challenging learning task due to the disparate domains of input and output;
- 3D volumetric representations bring potential quantization artifacts and require large memory for high voxel resolution;
### Contributions:
- Propose an end-to-end deep Semantic Hand Pose Regression network (SHPR-Net) for estimating hand poses from point clouds;
- Better fuses information from semantic segmentation network and regression network to achieve more representative features for hand pose estimation;
- Introduces a mechanism to deal with the challenges of geometric transformations by learning a transformation matrix for the input data and an inverse matrix for the output pose;
### Proposed Approach:
- Framework of SHPR-Net
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/34.png)
- Preprocessing
    * First convert all pixels in depth image to world coordinates to generate a point cloud.
    * Apply online random data augmentation strategy to increase generalization ability of the network: Rotation,scaling and translation to the point sets and corresponding annotated hand poses in training.
- Semantic Segmentation Network(SegNet)
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/35.png)
    * SegNet consists of three abstraction levels which extract features for local regions;
    * Derive semantic labels from the annotated hand pose for training(seeFig.2);
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/36.png)
- Hand Pose Regression Network(RegNet)
    * The hand pose regression network (RegNet) aims to directly estimate the 3D coordinates of hand pose from the input point set.
    * Compared with PointNet/PointNet++, RegNet goes further in two aspects: geometric transformation and semantic enhancement.
    * Incorporate two T-Nets to learn two matrices (T in and T out ) to transform the input points and output pose respectively;
    * To better fuse the information of SegNet, the predicted semantic probabilities are passed through a fully connected (fc) layer and then concatenated with the output of the first fc layer of RegNet. The fused features undergo another two fc layers to produce the predicted hand pose.
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/37.png)
### Experiment:
- Datasets: ICVL/NYU/MSRA
### Ablation Study:
- Impacts of the input and output transformations
    * The improvement is probably due to more model parameters brought by the T-Net;
    * Learning constrained transformation matrices for input and output space is an effective way to handle the geometric transformation for hand pose regression problem.
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/38.png)
- Impacts of semantic information
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/39.png)
    * These experiments demonstrate the effectiveness of our proposed strategy to incorporate semantic information into regression network;
- Impacts of point number
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/40.png)
    * To balance accuracy and computational complexity, choose N = 4096 and do not exploit more points.
- Impacts of multi-view point cloud fusion
    * The potentials to exploit multi-view data to boost the accuracy of hand pose estimation;
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/41.png)
### Future work：
- Future work may focus on designing a new backbone architecture to better leverage the properties of hand point clouds and hand poses.
