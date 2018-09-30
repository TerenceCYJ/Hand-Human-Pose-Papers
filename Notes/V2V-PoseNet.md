# 《V2V-PoseNet: Voxel-to-Voxel Prediction Network for Accurate 3D Hand and Human Pose Estimation from a Single Depth Map》
* Authors: Gyeongsik Moon, Ju Yong Chang, Kyoung Mu Lee, CVPR, 2018
## Summary：
- Background:
    * As for the task for 3D hand and human pose estimation from a single depth map, most methods directly regress the 3D coordinates via 2D CNNs. 
    * Weakness of 2D CNNs approaches: perspective distortion in the 2D depth map,  directly regressing 3D coordinates from a 2D image is a highly nonlinear mapping, which causes difficulty in the learning procedure.
- Contributions:
    * Firstly cast the problem of estimating 3D pose from a single depth map into a voxel-to-voxel prediction;
    * Validate the usefulness of the volumetric input and output representations by comparing the performance of each input type (i.e., 2D depth map and voxelized grid) and output type (i.e., 3D coordinates and per-voxel likelihood).
		
- Proposed Approach:
    * Overview: 
        * Input: a voxelized  grid (by reprojecting the points in the 3D space and discretizing the continuous space)
        * Output: the per-voxel likelihood for each keypoint (then warp to the real world coordinate)
        * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/11.png)
    * Input and output representation in 3D pose estimation:
         * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/12.png)
         * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/13.png)
    * Generating input of the proposed system
        * 1. Reproject each pixel of the 2D depth map to the 3D space;
        * 2. Discretize 3D space based on the pre-defined voxel size;
        * 3. Extract the target object by drawing the cubic box around the reference point;
    * V2V-PoseNet
        * Four kinds of building blocks: 
				□ volumetric basic block (volumetric convolution, volumetric batch normalization, and the activation function)
				□ volumetric residual block (extended from the 2D residual block)
				□ volumetric downsampling block (volumetric max pooling layer)
				□ volumetric upsampling block (volumetric deconvolution layer, volumetric batch normalization layer, and the activation function)
        * Network design: Figure 3
        * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/14.png)
- Experiment:
    * Dataset: ICVL/NYU/MSRA/HANDS 2017/ITOP Dataset
- Conclusion:
    * 3D representation and per-voxel likelihood estimation
        * Converting the input representation type from the 2D depth map to 3D voxelized form substantially improves performance;
        * Converting the output representation from the 3D coordinates to the per-voxel likelihood increases the performance significantly;
        * Voxel-to-voxel gives the best performance even with the smallest number of parameters; 
    * Refining localization of the target object
        * The refined reference points significantly boost the accuracy of our model.(See Table2)
    * Epoch ensemble. 
        * The epoch ensemble averages the estimations from several epochs. .(See Table2)
