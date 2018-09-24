# 《3D Convolutional Neural Networks for Efficient and Robust Hand Pose Estimation from Single Depth Images》
* Authors: Liuhao Ge, Hui Liang, Junsong Yuan, Daniel Thalmann, CVPR, 2017
## Summary：
- Background:
    * Image based features extracted by 2D CNNs are not directly suitable for 3D hand pose estimation due to the lack of 3D spatial information. 
    * Categories of HAND POSE ESTIMATION: model-driven approach, data-driven approach, hybrid approach.
- Contributions:
    * The 3D CNN can directly regress 3D joint locations from 3D features in a single pass;
    * Can meet the real-time requirement for hand pose estimation;
    * Robust to variations in hand sizes and global orientations, since we perform 3D data augmentation on the training set;
- Proposed Approach:
    * Volumetric Representation:
        * Objective: enerate 3D volumes representing the hand in 3D space as raw as possible from the depth image in real-time;
        * Apply the projective Directional TSDF (D-TSDF) in the camera’s coordinate system;
        * Steps: 
           * Build an axis-aligned bounding box (minimum bounding box ) for 3D hand points;
           * Set 3D volume's center/faces and voxel's edge length w.r.t bounding box;
           * Balance the volume resolution value with computational cost;
    * Network Architecture:
        * Input: three volumes of the projective D-TSDF; 
        * Output: a column vector containing 3× K elements corresponding to the K 3D hand joint relative locations in the volume;
        * Three 3D convolutional layers  +  three fully-connected layers;
    * 3D Data Augmentation:
        * Directly rotate and stretch the hand point cloud in 3D space;
      ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/4.png)
      ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/5.png)
- Experiment:
    * Dataset: MSRA and NYU dataset
## Strengths / Novelties：
- The first work that applies such a 3D CNN in hand pose estimation;
## Weaknesses / Notes：
