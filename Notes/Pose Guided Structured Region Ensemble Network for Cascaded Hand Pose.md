# 《Pose Guided Structured Region Ensemble Network for Cascaded Hand Pose》
* Authors: Xinghao Chena, Guijin Wanga, Hengkai Guob, Cairong Zhang, arXiv, 2017
* Keywords: Hand Pose Estimation, Convolutional Neural Network, Human Computer Interaction, Depth Images

### Background:
- Few of prior works have paid attentions to extracting more optimal and representative features of CNN;
### Contributions:
- Present a novel feature extraction method under the guidance of previous predicted hand pose to get optimal and representative features for hand pose estimation;
- Present a hierarchical method to fuse features of different joints according to the topology of hand;
### Proposed Approach: Pose Guided Structured Region Ensemble Network
- Overview
    * Init-CNN predicts an initial hand pose, which is used as the initialization of the cascaded framework;
    * Takes a previously estimated hand pose and the depth image as input;
    * The depth image is fed into a CNN to generate feature maps; Feature regions are extracted from these feature maps under the guidance of the input hand pose;
    * Features from di erent joints are hierarchically integrated using the structured connection to regress the refined hand pose;
    * The refined hand pose obtained by proposed Pose-REN and will be used as the guidance in next stage.
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/27.png)
- Pose Guided Region Extraction
    * Extract  feature regions from the feature maps for each joint using the guidance of previously estimated hand pose.
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/28.png)
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/29.png)
- Structured Region Ensemble
    * Adopt hierarchically structured region ensemble strategy to better model the constraints of hand joints;
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/30.png)
- Training
    * First trained the Init-CNN to obtain initial hand pose;
    * After that, use the weights of trained Init-CNN to initialize Pose-REN and train the network;
### Experiment:
- Dataset: ICVL/NYU/MSRA
### Ablation Study:
- Effect of the Number of Iteration T:
    * Choose the number of iteration as T = 3
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/31.png)
- Effect of Pose Guided Region Extraction:
    * One of the contributions of the proposed method is to extract feature regions under the guidance of hand pose from previous stage;
    * The method both performs better than REN that adopts grid region ensemble, indicating
		the contributions of pose guided region extraction strategy;
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/32.png)
- Effect of Structured Region Ensemble
    * Proposed method performs better than Ours w-o structure, which illustrates the e ectiveness of the hierarchically structured region ensemble strategy;
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/33.png)
- Effect of the Initialization
    * The model trained on our initialization greatly generalize to other initializations;
    * For a very poor initialization, our proposed method can still obtain satisfying results by training a model using this initialization.
### Strengths / Novelties：
- Upon an iterative re nement procedure, the proposed method takes a previously estimated pose as input and predicts a more accurate result in each iteration;
- Proposed discriminative method and does not rely on any pre-defined hand model;
- The Pose-REN is a common framework that can easily be compatible with any existing methods by using them to produce initial estimations for Pose-REN.
### Weaknesses / Future Work：
- In future work, intend to further improve our method for robust and accurate 3D hand pose estimation when hands are interacting with other hands or objects; 
- Would like to research on integrating hand detection and hand pose estimation into a uniffed framework, based on Faster R-CNN or Mask R-CNN;

