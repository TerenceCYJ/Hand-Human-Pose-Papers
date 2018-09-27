# 《Real-time 3D Hand Pose Estimation with 3D Convolutional Neural Networks》
* Authors: Liuhao Ge, Hui Liang, Junsong Yuan, Daniel Thalmann, TPAMI, 2018
* Keywords: 3D hand pose estimation, 3D convolutional neural networks, deep learning
## Summary：
- Contributions:
    * Leveraging the complete hand surface as intermediate supervision for learning 3D hand pose from depth images;
    * Experimental results have shown that the 3D deep dense network can achieve better performance than the 3D shallow plain network;
- Proposed Approach:
    * Volumetric Representations:
        * Objective: generate 3D volumes providing sufficient and meaningful information of the hand in 3D space from the depth image in real-time;
        * The input depth image of hand is first converted to a set of 3D points;
        * Apply the projective Directional TSDF (D-TSDF) to encode more information in the volumetric representation;
    * 3D CNN: 
        * Architecture: 3D Shallow Plain Network & 3D Deep Dense Network;
        
      ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/6.png)
    * Hand Surface Completion
        * Leverage the complete hand surface as intermediate supervision for learning 3D hand pose from depth images;
        * Apply the 3D U-Net architecture for estimating the complete hand surface from the captured partial hand surface;
        
      ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/7.png)
- Others:
    * 3D Data Augmentation: directly rotate and stretch the hand points in 3D space;
    * Visualizing 3D CNN: From low layer (L1) to high layer (L3), neurons can capture patterns from local to global;
- Experiment:
    * Datasets: MSRA、NYU、ICVL hand pose dataset.
    * Self-comparison: 
        * Choice of Volume Resolution
        * Choice of Volume Types
        * Evaluation of Data Augmentation
        * 2D CNNs Versus 3D CNNs
        * Shallow Network Versus Deep Network
    * Comparison with state-of-the-art
## Strengths / Novelties：
- 3D CNN can directly regress 3D joint locations from 3D features in a single pass;
- 3D CNN  designed in this paper can run at real-time speed on a single GPU;
- Robust to variations in hand sizes and global orientations;
## Weaknesses / Notes：
