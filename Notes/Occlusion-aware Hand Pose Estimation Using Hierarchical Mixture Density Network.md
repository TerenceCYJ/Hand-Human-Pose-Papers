# 《Occlusion-aware Hand Pose Estimation Using Hierarchical Mixture Density Network》
* Authors: Qi Ye, Tae-Kyun Kim, ECCV, 2018
* Keywords: 3D Hand Pose Estimation, Occlusion, Multi-valued Mapping, Convolutional Neural Network, Mixture Density Network
## Summary：
- Background:
    * Discriminative methods have been very successful in the settings of third-person viewpoints, but fail to handle occlusions frequently encountered in egocentric viewpoints;
    * The existing methods do not address multi-modalities nor do not model the difference in distributions of visible and occluded joints;
    * Mixture density networks (MDN) were first proposed to enable neural networks to overcome the limitation of the mean squared error function by producing a probability distribution;
- Contributions:
    * Apply MDN to model th.e hand pose space when multiple modes
		exist due to occlusion
- Proposed Approach: Hierarchical Mixture Density Network
    * Model Representation: a two-level hierarchy 
        * Top-level: takes the visibility label.
        * Bottom-level: switches between a uni-modal distribution and a multi-modal distribution, depending on the joint visibility.
    * Architecture:
        * Input of the CNN is an image
        * Outputs are the HMDN parameters: w,µ,σ,ǫ,s,π.
        * The output parameters consist of three parts. w is the visibility probability in the Bernoulli distribution, µ,σ for the uni-modal Gaussian in single Gaussian distribution, and ǫ,s,π for the Gaussian Mixture Model(GMM).
        * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/16.png)
- Experiment:
    * Datasets:
        * ICVL, NYU, MSHD
        * BigHand: the egocentric subset, the third-person viewpoint subset 
        * Augment the egocentric subset using the articulations of the third-person view dataset, and use it called EgoBigHand for experiments.
    * Training:
        * Use the negative logarithmic likelihood as the loss function.
        * Use the samples drawn from the estimated distribution.
    * Testing:
        * When an image xnis fed into the network, the prediction for the d-th joint location is diverted to di.erent branches according to the prediction of the visibility probability.

## Strengths / Novelties：
- Hierarchical mixture density networks (HMDN) is the first solution that has its estimation in the form of a conditional probability distribution with the awareness of occlusions in 3D hand pose estimation.
- HMDN successfully captures the distributions of visible and occluded joints, and significantly outperforms prior work in terms of hand pose estimation accuracy.

## Weaknesses / Notes：
- Further incorporate the temporal dependency using offline priors or learning it with the part regression in the LSTM framework.
