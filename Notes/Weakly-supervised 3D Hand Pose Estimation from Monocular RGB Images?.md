# 《Weakly-supervised 3D Hand Pose Estimation from Monocular RGB Images?》
* Authors: Yujun Cai, Liuhao Ge, Jianfei Cai, Junsong Yuan, ECCV Oral, 2018
* Keywords: 3D hand pose estimation, weakly-supervised methods, depth regularizer
## Summary：
- Contributions:
    * introduce the weakly supervised problem of leveraging lowcost depth maps during training for 3D hand pose estimation from RGB images;
    * introduce a depth regularizer supervised by the easily captured depth images, which considerably enhances the estimation accuracy;
- Proposed Approach:
    * Overview: 
        * Architecture: a 2D pose estimation network (convolutional pose machines - CPM), a 3D regression network, and a depth regularizer;
        * Input: a cropped single RGB image containing human hand with certain gesture;
        * Output: the 2D heatmap and the corresponding depth of each joint (3D joint locations in camera coordinate system);
        * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/1.png)
    * 2D Pose Estimation Network:
        * encoder-decoder architecture which is fully convolutional with outputs K low-resolution heatmaps;
        * predict each joint by applying the MMSE (Minimum mean square error given a posterior) estimator;
    * Regression Network:
        * Objective：infer the depth of each joint from the obtained 2D heatmap；
        * Inputs：the intermediate image evidence in 2D pose estimation network concatenated with the predicted 2D heatmaps；
        * Structure：two convolutional layers and three fully-connected layers；
        * infer a scale-invariant and translation-invariant representation of joint depth；
    * Depth Regular:
        * Objective：take the easily-captured depth images as an implicit constraint of physical structures that can be applied to both weakly-supervised and fully-supervised situations；
        * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/2.png)
- Experiment:
    * Publicly Dataset：RHD(Rendered Hand Pose Dataset) and STB(a real-world dataset from Stereo Hand Pose Tracking Benchmark)；
    * Quantitative Result：Weak supervision + Fully-supervised
## Strengths / Novelties：
* a large real-world hand dataset with full 3D annotations is often one of the major bottlenecks ==》adapt weakly labeled real-world dataset from fully-annotated synthetic dataset with the aid of low-cost depth images；
* the first exploration of leveraging depth maps to compensate the absence of entire 3D annotations；
## Weaknesses / Notes：
