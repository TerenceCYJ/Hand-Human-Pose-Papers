# 《Dense 3D Regression for Hand Pose Estimation》
* Authors: Chengde Wan, Thomas Probst, Luc Van Gool, Angela Yao, CVPR, 2018
* Keywords: Fusion scheme between 2D detection and 3D regression

## Contributions
- Formulate 3D hand pose estimation as a dense regression through a pose re-parameterization that can leverage both 2D surface geometric and 3D coordinate properties;
- Non-parametric post-processing method aggregating pixel-wise estimates to 3D joint coordinates;
- Leverage both the 2D and 3D properties of a depth map to formulate hand pose estimation as a pixel-wise regression problem;

## Proposed Approach
- Method
    * From a 2D perspective, treat the depth map as a 2D surface embedded in 3D and use a convolutional neural network(CNN) composed of 2D convolutional layers to capture surface local geometric patterns;
    * From a 3D perspective, the depth map can also be regarded as a set of 3D points. And use a CNN to estimate a dense vector field of offsets for each joint of hand;
    * Re-parameterize the joint offset as a 3D heat map and a directional unit vector and solve for the two via detection and regression respectively;
- Pose Parameterization
    * Decompose the 3D offset vector into two components: a 3D heat map (estimated via detection), and a directional unit vector (via regression);
    * In addition, estimate the joint’s 2D projection as a heatmap (adds robustness to the local estimate);
- Network Architecture
    * Use the hourglass network as the backbone;
    * The 2D and 3D joint heat maps and the unit vector fields are estimated by network cascades:
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/44.png)
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/45.png)

## Experiment
- Use two network stacks and have an average run time of 36ms per image (27.8FPS) on a single NVIDIA Titan X GPU card;
## Ablation Study
- Does 2D joint detection help with 3D regression?
    * There is only a minor improvement of 0.16mm in terms of the average joint error from direct coordinate regression to detection+coordinate regression;
    * While 2D detection may help in learning a better feature map, coupling 2D detection together with 3D regression does not solve the inherent problems of 3D regression, e.g., translation variance and inability to generalize through combining local evidence.
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/46.png)
- Impact of fusion strategies
    * 2D detection provides a more accurate estimate than coordinate regression;
    * Fusing the 2D detection heat maps as input for coordinate regression, conducts model-based tracking based on inverse kinematics to recover the 3D pose; This validates the effectiveness of our proposed method in handling depth ambiguities arising from the severe self occlusions in the hand;
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/47.png)
- Impact of offset re-parameterization
    * As is shown in Fig. 3, pixel-wise dense estimation out-performs holistic regression method and validates the benefits of regressing point-wise 3D offsets;
    * Decomposing the 3D offsets into the joint 3D heat map and offset direction and regressing the two in a cascaded way is easier to learn than directly regressing the offsets;
    * Setting the offset vector to zero for outlier points instead of excluding them from the loss makes the estimation more robust to errors in regression during testing;

## Strengths / Novelties：
- Estimate an offset vector between depth points and hand joints, instead of directly regressing 3D joint coordinates from the depth map;
- Provides a better fusion scheme between 2D detection and 3D regression;
## Weaknesses / Future work：
- As future work, plan to further extend our method for 3D pose estimation from RGB inputs as well as for hands grasping objects.
