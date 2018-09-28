# 《Point-to-Point Regression PointNet for 3D Hand Pose Estimation》
* Authors: Liuhao Ge , Zhou Ren, Junsong Yuan, ECCV, 2018
* Keywords: 3D Hand Pose Estimation
## Summary：
- Contributions:
    * Propose a point-to-point regression method for 3D hand pose estimation in single depth images;
    * Apply the stacked network architecture to the hierarchical PointNet for point-to-point regression;
- Proposed Approach:
    *  Overview：
      ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/8.png)
    * Point Cloud Preprocessing:
        * Convert hand depth image to a set of 3D points using the depth camera's intrinsic parameters;
        * Downsampled to N points; Transform the 3D points into the OBB C.S; Denote the downsampled and normalized 3D point set in OBB C.S. ;
    * Point Cloud based Representation for 3D Hand Pose:
        * Traditional direct regression approaches that require to learn a highly non-linear mapping；
        * This method aims at generating point-wise estimations of hand joint locations from the point cloud, which is able to better utilize the local evidence and better utilize the 3D spatial information in the depth image;
      ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/9.png)
    * Network Architecture: hierarchical PointNet for learning heat-maps and unit vector elds on 3D point cloud;
        * Input: a set of 3-dim coordinates with 3-dim input features;
        * Using 3 set abstraction levels to extract a global feature vector from point cloud;
        * Using 3 feature propagation levels to propagate the global feature to point features for original points;
        * Using per-point MLP to concatenat the interpolated features and points with the corresponding point features in the set             ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/10.png)
    * Hand Pose Inference:
        * infer the 3D hand pose from the heat-maps and the unit vector fields estimated by the last hierarchical PointNet module;
    * Post-processing:
        * add three fully-connected layers for direct hand pose regression to the pre-trained two-stacked hierarchical PointNet to save the inference time.
        * explicitly constrain the estimated 3D hand pose on a lower dimensional space learned by principal component analysis (PCA).
- Experiment:
    * Datasets: NYU/ICVL/MSRA dataset.
## Strengths / Novelties：
- infer 3D hand joint locations from the estimated heat-maps and unit vector fields using weighted fusion;
- apply the stacked network architecture for the hierarchical PointNet, which allows repeated bottom-up and top-down inference on point cloud and is able to further boost the performance. 
## Weaknesses / Notes：
