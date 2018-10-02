# 《Augmented Skeleton Space Transfer for Depth-based Hand Pose Estimation》
* Authors: Seungryul Baek, Kwang In Kim, Tae-Kyun Kim, CVPR, 2018
* Keywords: Hand pose generator (HPG) and estimator (HPE) combination 
## Summary：
- Contributions:
    * A new hand pose generator (HPG) and estimator (HPE) combination that enables to exploit both existing paired skeletons and depth map entries and newly synthesized depth maps in a single unified framework;
    * Refines the HPE prediction during testing by generating multiple pose hypotheses and combining them using HPD and HPG as a prior;
- Introduction:
    * Primary goal is enrich existing datasets by augmenting them / proposed algorithm focuses on the capability of transferring the augmented skeletons to depth maps. 
- Proposed Approach: Pose estimation by skeleton set augmentation
    * Skeleton set augmentation: Enlarge its skeleton space coverage by adding variations in viewpoints(applying 3D rotations)  and shapes;
    * Transferring skeletons to depth maps: 
        * Hand pose generator (HPG): synthesizes a depth map given the input skeleton parameters by conditional GAN architecture;
        * Hand pose discriminator (HPD): construct auxiliary models that provide feedback on the quality of synthesized data;
	        * Depth hand pose discriminator (HPDX): is the same as the standard GAN discriminator;
	        * Skeleton hand pose discriminator (HPDY): is to decide whether the estimated finger joints conform the human skeleton model;
    * Training HPG and HPE
	        * The goal is to jointly train HPG and HPE by fully exploiting the paired data as well as the augmented unpaired data;
         * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/15.png)
    * Refining predictions at testing
- Experiment:
    * Training: Combining and jointly training HPG, HPE, and HPD enable the automatic transfer of the augmented skeletons to depth maps.
    * Testing: Synthesize multiple hand pose hypotheses out of the initial HPE prediction, and generate the final refined prediction by combining them using the HPG and HPD as a prior.
## Strengths / Novelties：
- The key idea is to synthesize data in the skeleton space (instead of doing so in the depth-map space);
- Inspired from the recent success of 2D/3D image generation, this paper train the hand pose generator (HPG) that transfers input skeletons to corresponding depth maps. As in generative adversarial networks (GANs), this paper train the second, hand pose discriminator (HPD) that distinguishes real depth maps from these synthesized by the HPG. 
## Weaknesses / Notes：
