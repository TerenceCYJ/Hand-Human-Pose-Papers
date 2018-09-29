# 《Hand PointNet: 3D Hand Pose Estimation using Point Sets》
* Authors：Liuhao Ge, Yujun Cai, Junwu Weng, Junsong Yuan, CVPR, 2018
* Video：https://www.youtube.com/watch?v=-eiZYOo8cWc
* Code：https://sites.google.com/site/geliuhaontu/HandPointNet.zip?attredirects=0&d=1
## Summary：
- Contributions:
    * estimate 3D hand joint locations directly from 3D point cloud;
    * normalize the sampled 3D points in an oriented bounding box without applying any additional network to transform the hand point cloud;
    * refine the fingertip locations with a basic PointNet;
- Proposed Approach:
      ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/3.png)
    * Overview：
        * Input: a depth image containing a hand; 
        * Output: a set of 3D hand joint locations in the camera coordinate system; 
    * PointNet:
        * Basic PointNet: extract discrimination features of the point cloud;
        * Hierarchical PointNet: better generalization ability due to its hierarchical feature extraction architecture than basic PointNet;
    * OBB-based Point Cloud Normalization:
        * The large variation in global orientation of the hand is one challenge;
        * A simple yet effective method to normalize the 3D hand point cloud in OBB; Perform PCA on input points to get the orientation of OBB; Transform original points in camera C.S. into OBB C.S.;
    * Hand Pose Regression Network:
        * Input: a set of normalized points;
        * Output: 3D joints
    * Fingertip Refinement Network:
        * To further improve the estimation accuracy of fingertip locations; only refine fingertips for straightened fingers;
        * Input: K nearest neighboring points of the estimated fingertip location;
        * Output: the refined 3D location of the fingertip;
- Experiment:
    * Dataset: NYU、MSRA and ICVL dataset.
## Strengths / Novelties：
- the first work that regresses 3D hand joint locations directly from the 3D point cloud using a deep neural network；
## Weaknesses / Notes：
