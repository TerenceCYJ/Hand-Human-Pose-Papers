# 《Depth-Based 3D Hand Pose Estimation:From Current Achievements to Future Goals》
* Authors: Shanxin Yuan .etc, CVPR, 2018
### Evaluated methods:
- 2D CNN vs. 3D CNN. 
    * The input of 3D CNN can be a 3D voxel grid,or a projective D-TSDF volume; 
- Detection-based vs. Regression-based. 
    * Detection-based methods produce a probability density map for each joint;
    * Regression-based methods directly map the depth image to the joint locations or the joint angles of a hand model.
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/17.png)
- Hierarchical models:
    * Divide the pose estimation problem into sub-tasks by a hierarchically structured CNN；
    * Divide the hand joints either by finger or by joint type;
- Structured methods
    * Embed physical hand motion constraints into the model (in the CNN model or in the loss function);
- Multi-stage methods
    * Propagate results from each stage to enhance the training of the subsequent stages; 
### Results：
- Consider joint visibility, seen vs. unseen subjects, hand view point distribution, articulation distribution, and per-joint accuracy;
- Mean errors (in mm) for single frame pose estimation:
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/18.png)
- Single frame pose estimation
    * Annotation error: a mean value of 2.8 mm and a standard deviation of 0.5 mm;
    * Analysis by occlusion and unknown subject:
	    * The error for unseen subjects is significantly larger than for seen subjects;
	    * The error for visible joints is smaller than for occluded joints;
	    * 3D CNN outperform 2D CNN(See the bottom-left plot of Figure 4);
	    * Detection-based methods outperform regression-based ones;(see the top-right plot of Figure 4)
	    * Hierarchical constraints can help in the case of occlusion(see the bottom-right plot of Figure 4);
	    * Cascaded methods work better than single-stage methods, see the bottom-right plot of Figure 4. 
	    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/19.png)
    * Analysis by number of occluded joints:
	    * The average error decreases nearly monotonously for increasing numbers of visible joints.
    * Analysis based on view point:
	    * The view point is defined as the angle between the palm and camera directions;
	    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/20.png)
    * Analysis based on articulation:
	    * Evaluate the effect of hand articulation on estimation accuracy, measured as the average of 15 finger flexion angles;
	    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/21.png)
    * Analysis by joint type:
	    * For seen subjects, along the kinematic hand structure from the wrist to finger tips, occluded joints have increasingly larger errors, reaching 14 mm in the finger tips;
	    * Visible joints of unseen subjects have larger errors (10-13 mm) than that of seen subjects;
	    * Occluded joints of unseen subjects have the largest errors, with a relatively smaller error for the palm, and larger errors for finger tips;
	    * Middle and ring fingers tend to have smaller errors in MCP and PIP joints than other fingers. One reason may be that the motion of these fingers is more restricted; The thumb’s MCP joint has a larger error than for other fingers, because it tends to have more discrepancy among different subjects.
	    * Two conclusions:
		    * All the top performers have difficulty in generalizing to hands from unseen subjects;
		    * Occlusions have more effect on finger tips than other joints. 
	    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/22.png)
- Hand pose tracking
- Hand object interaction
    * Current state-of-the-art methods have difficulty generalizing to the hand-object interaction scenario;
    * CNN-based segmentation can better preserve structure than image processing operations.
### Conclusion:

- (1) 3D volumetric representations used with a 3D CNN show high performance；
- (2) Detection-based methods tend to outperform regression-based methods; Regression-based methods can achieve good performance using explicit spatial constraints(e.g., bone structure); Regression-based methods perform better in extreme view point cases, where severe occlusion occurs;
- (3) Explicit modeling of structure constraints and spatial relation between joints can significantly narrow the gap between errors on visible and occluded joints;
- (4) Discriminative methods still generalize poorly to unseen hand shapes. **Integrating hand models with better generative capability may be a promising direction**.
- (5) Errors remain large for extreme view points, e.g.,view point range of [0,10], where the hand is facing away from the camera. Multi-stage methods tend to perform better in these cases.
- (6) Current methods perform well on single hand pose estimation when trained on a million-scale dataset, but have difficulty in generalizing to hand-object interaction. Two directions seem promising:
    * **i. Designing better hand segmentation methods.**
    * **ii. Training the model with large datasets containing hand-object interaction.**
