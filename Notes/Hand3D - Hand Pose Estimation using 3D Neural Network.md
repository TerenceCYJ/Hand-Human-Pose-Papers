# 《Hand3D: Hand Pose Estimation using 3D Neural Network》
* Authors: Xiaoming Deng, Shuo Yang, Yinda Zhang, Ping Tan, Liang Chang, Hongan Wang, arXiv, 2017
### Background:
- Regression models either require a careful initial alignment or being sensitive to the predefined bone length. 
- Available datasets often contain biased hand pose from a few number of subjects. Therefore, data augmentation is important. 
### Contributions:
- Propose a 3D network to directly estimate the 3D hand pose;
- Perform data augmentation:
    * Use a 3D FCN to refine the TSDF which completes missing depth;
    * Learn poses from real datasets and transfer them to synthetic CAD models;
### Proposed Approach:
- Overviews：
    * Depth image --> Build a reference coordinate at the center of mass (COM) of the foreground region --> A truncated signed distance function (TSDF) representation --> TSDF refinement network(which removes the artifacts caused by noisy and missing depth) --> 3D pose network to estimate the 3D location.
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/23.png)
- 3D Pose Estimation Network:
    * Hand pose parametrization
    * 3D volumetric representation
	    * Convert the input depth image into a truncated signed distance function(TSDF) representation.
	    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/24.png)
    * Hand shape refinement
	    * Taking the TSDF of the raw depth as input, we train a 3D fully convolutional network(FCN) to estimate the TSDF of the combined depth. 
	    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/25.png)
    * Pose estimation network
	    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/26.png)
- Data Augmentation:
    * Pose parametrization for synthetic data: 
	    * Use the angle between two connecting bones on each joint to represent the hand;
	    * Changing the bone length while maintaining these angles is likely to produce natural looking hand poses;
    * Learning pose from real dataset: 
	    * optimize the parametrized hand pose p for the smallest forward kinematics cost, which measures the pairwise distances between the hand joint positions in hand model and the corresponding ground truth hand joints.
    * Transfer pose to synthetic data:
	    * Encode the recovered hand pose into a standard Biovision hierarchical data(BVH) file(consists of the position of root joint, relative angles of each joint, and canonical bone lengths);
	    * Modify the relative offsets in the BVH file to generate models with different bone lengths;
	    * Attempted to generate synthetic data with different skeleton sizes and different camera poses in building data augmentation pipeline;
### Experiment:
- Dataset: NYU/ICVL
