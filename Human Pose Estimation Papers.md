# Notes of Human Pose & Shape Estimation

## Table of Contents
 - [arXiv Papers](#arxiv-papers)
 - [Journal Papers](#journal-papers)
 - [Conference Papers](#conference-papers)
   - 2019: [CVPR](#2019-cvpr), [ICCV](#2019-iccv), [Others](#2019-others)
   - 2018: [CVPR](#2018-cvpr), [ECCV](#2018-eccv), [Others](#2018-others)
   - 2017: [CVPR](#2017-cvpr), [ICCV](#2017-iccv), [Others](#2017-others)
   - [Before 2016](#before-2016)
 - [Theses](#theses)
 - [Other Related Papers](#other-related-papers)
 - [Datasets](#datasets)
 - [Popular implementations](#popular-implementations)
   - [PyTorch](#pytorch)
   - [TensorFlow](#tensorflow)
   - [Torch](#torch)
   - [Others](#others)
 
 ## Basics
- [Human Pose Estimation 101](https://github.com/cbsudux/Human-Pose-Estimation-101)
- [awesome-human-pose-estimation](https://github.com/cbsudux/awesome-human-pose-estimation)
## arXiv Papers
##### [\[arXiv:1901.06792\]](https://arxiv.org/abs/1901.06792) Semantic Image Networks for Human Action Recognition. [\[PDF\]](https://arxiv.org/pdf/1901.06792.pdf)
_Sunder Ali Khowaja, Seok-Lyong Lee_
##### [\[arXiv:1812.10550\]](https://arxiv.org/abs/1812.10550) Learning to Recognize 3D Human Action from A New Skeleton-based Representation Using Deep Convolutional Neural Networks. [\[PDF\]](https://arxiv.org/pdf/1812.10550.pdf)
_Huy-Hieu Pham, Louahdi Khoudour, Alain Crouzil, Pablo Zegers, Sergio A. Velastin_
##### [\[arXiv:1812.10766\]](https://arxiv.org/abs/1812.10766) SMPLR: Deep SMPL reverse for 3D human pose and shape recovery. [\[PDF\]](https://arxiv.org/pdf/1812.10766.pdf)
_Meysam Madadi, Hugo Bertiche and Sergio Escalera_
##### [\[arXiv:1807.02131\]](https://arxiv.org/abs/1807.02131) 3D Human Action Recognition with Siamese-LSTM Based Deep Metric Learning. [\[PDF\]](https://arxiv.org/pdf/1807.02131.pdf)
_Seyma Yucer, Yusuf Sinan Akgul_
##### [\[arXiv:1806.11230\]](https://arxiv.org/abs/1806.11230) Human Action Recognition and Prediction: A Survey. [\[PDF\]](https://arxiv.org/pdf/1806.11230.pdf)
_Yu Kong, Yun Fu_


## Journal Papers

## Conference Papers
### 2019 ICCV
##### DenseRaC: Joint 3D Pose and Shape Estimation by Dense Render-and-Compare.[\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Xu_DenseRaC_Joint_3D_Pose_and_Shape_Estimation_by_Dense_Render-and-Compare_ICCV_2019_paper.pdf) *(Oral)*
_Yuanlu Xu, Song-Chun Zhu, Tony Tung_
##### A Neural Network for Detailed Human Depth Estimation From a Single Image.[\[Project Page\]]() [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Tang_A_Neural_Network_for_Detailed_Human_Depth_Estimation_From_a_ICCV_2019_paper.pdf) *(Oral)*
_Sicong Tang, Feitong Tan, Kelvin Cheng, Zhaoyang Li, Siyu Zhu, Ping Tan_
##### Not All Parts Are Created Equal: 3D Pose Estimation by Modeling Bi-Directional Dependencies of Body Parts. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Wang_Not_All_Parts_Are_Created_Equal_3D_Pose_Estimation_by_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Wang_Not_All_Parts_ICCV_2019_supplemental.pdf) *(Oral)*
_Jue Wang, Shaoli Huang, Xinchao Wang, Dacheng Tao_
##### xR-EgoPose: Egocentric 3D Human Pose From an HMD Camera. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Tome_xR-EgoPose_Egocentric_3D_Human_Pose_From_an_HMD_Camera_ICCV_2019_paper.pdf)  *(Oral)*
_Denis Tome, Patrick Peluse, Lourdes Agapito, Hernan Badino_

##### Pose-Aware Multi-Level Feature Network for Human Object Interaction Detection. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Wan_Pose-Aware_Multi-Level_Feature_Network_for_Human_Object_Interaction_Detection_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Wan_Pose-Aware_Multi-Level_Feature_ICCV_2019_supplemental.pdf) [\[Code\\]](https://github.com/bobwan1995/PMFNet) *(Oral)*
_Bo Wan, Desen Zhou, Yongfei Liu, Rongjie Li, Xuming He_
##### TRB: A Novel Triplet Representation for Understanding 2D Human Body. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Duan_TRB_A_Novel_Triplet_Representation_for_Understanding_2D_Human_Body_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Duan_TRB_A_Novel_ICCV_2019_supplemental.zip) *(Oral)*
_Haodong Duan, Kwan-Yee Lin, Sheng Jin, Wentao Liu, Chen Qian, Wanli Ouyang_
##### Learning Trajectory Dependencies for Human Motion Prediction. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Mao_Learning_Trajectory_Dependencies_for_Human_Motion_Prediction_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Mao_Learning_Trajectory_Dependencies_ICCV_2019_supplemental.pdf) [\[Code\\]](https://github.com/wei-mao-2019/LearnTrajDep) *(Oral)*
_Wei Mao, Miaomiao Liu, Mathieu Salzmann, Hongdong Li_
##### Cross-Domain Adaptation for Animal Pose Estimation. [\[Dataset\]](https://www.jinkuncao.com/animalpose) [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Cao_Cross-Domain_Adaptation_for_Animal_Pose_Estimation_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Cao_Cross-Domain_Adaptation_for_ICCV_2019_supplemental.pdf) *(Oral)*
_Jinkun Cao, Hongyang Tang, Hao-Shu Fang, Xiaoyong Shen, Cewu Lu, Yu-Wing Tai_

##### DeepHuman: 3D Human Reconstruction From a Single Image. [\[Project Page\]](http://www.liuyebin.com/deephuman/deephuman.html) [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Zheng_DeepHuman_3D_Human_Reconstruction_From_a_Single_Image_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Zheng_DeepHuman_3D_Human_ICCV_2019_supplemental.pdf)  *(Oral)*
_Zerong Zheng, Tao Yu, Yixuan Wei, Qionghai Dai, Yebin Liu_
##### Learnable Triangulation of Human Pose.[\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Iskakov_Learnable_Triangulation_of_Human_Pose_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Iskakov_Learnable_Triangulation_of_ICCV_2019_supplemental.zip) [\[Code\\]](https://github.com/karfly/learnable-triangulation-pytorch)  *(Oral)*
_Karim Iskakov, Egor Burkov, Victor Lempitsky, Yury Malkov_
##### Distill Knowledge From NRSfM for Weakly Supervised 3D Pose Learning. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Wang_Distill_Knowledge_From_NRSfM_for_Weakly_Supervised_3D_Pose_Learning_ICCV_2019_paper.pdf)
_Chaoyang Wang, Chen Kong, Simon Lucey_
##### TexturePose: Supervising Human Mesh Estimation With Texture Consistency. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Pavlakos_TexturePose_Supervising_Human_Mesh_Estimation_With_Texture_Consistency_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Pavlakos_TexturePose_Supervising_Human_ICCV_2019_supplemental.pdf) [\[Code\\]](https://github.com/geopavlakos/TexturePose) 
_Georgios Pavlakos, Nikos Kolotouros, Kostas Daniilidis_
##### Markerless Outdoor Human Motion Capture Using Multiple Autonomous Micro Aerial Vehicles.[\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Saini_Markerless_Outdoor_Human_Motion_Capture_Using_Multiple_Autonomous_Micro_Aerial_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Saini_Markerless_Outdoor_Human_ICCV_2019_supplemental.zip) [\[Code\\]](https://github.com/robot-perception-group/Aircap_Pose_Estimator) 
_Nitin Saini, Eric Price, Rahul Tallamraju, Raffi Enficiaud, Roman Ludwig, Igor Martinovic, Aamir Ahmad, Michael J. Black_
##### Learning to Reconstruct 3D Human Pose and Shape via Model-fitting in the Loop. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Kolotouros_Learning_to_Reconstruct_3D_Human_Pose_and_Shape_via_Model-Fitting_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Kolotouros_Learning_to_Reconstruct_ICCV_2019_supplemental.pdf) [\[Code\\]](https://github.com/nkolot/SPIN)
_Nikos Kolotouros, Georgios Pavlakos, Michael J. Black, Kostas Daniilidis_
##### Moulding Humans: Non-Parametric 3D Human Shape Estimation From Single Images. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Gabeur_Moulding_Humans_Non-Parametric_3D_Human_Shape_Estimation_From_Single_Images_ICCV_2019_paper.pdf)
_Valentin Gabeur, Jean-Sebastien Franco, Xavier Martin, Cordelia Schmid, Gregory Rogez_
##### 3DPeople: Modeling the Geometry of Dressed Humans. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Pumarola_3DPeople_Modeling_the_Geometry_of_Dressed_Humans_ICCV_2019_paper.pdf)  
_Albert Pumarola, Jordi Sanchez-Riera, Gary P. T. Choi, Alberto Sanfeliu, Francesc Moreno-Noguer_
##### Optimizing Network Structure for 3D Human Pose Estimation. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Ci_Optimizing_Network_Structure_for_3D_Human_Pose_Estimation_ICCV_2019_paper.pdf)
_Hai Ci, Chunyu Wang, Xiaoxuan Ma, Yizhou Wang_
##### Exploiting Spatial-Temporal Relationships for 3D Pose Estimation via Graph Convolutional Networks. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Cai_Exploiting_Spatial-Temporal_Relationships_for_3D_Pose_Estimation_via_Graph_Convolutional_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Cai_Exploiting_Spatial-Temporal_Relationships_ICCV_2019_supplemental.pdf)
_Yujun Cai, Liuhao Ge, Jun Liu, Jianfei Cai, Tat-Jen Cham, Junsong Yuan, Nadia Magnenat Thalmann_
##### Resolving 3D Human Pose Ambiguities With 3D Scene Constraints. [\[Project Page\]](https://prox.is.tue.mpg.de/) [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Hassan_Resolving_3D_Human_Pose_Ambiguities_With_3D_Scene_Constraints_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Hassan_Resolving_3D_Human_ICCV_2019_supplemental.pdf) [\[Code\\]](https://github.com/MohameHassan/prox)
_Mohamed Hassan, Vasileios Choutas, Dimitrios Tzionas, Michael J. Black_
##### Tex2Shape: Detailed Full Human Body Geometry From a Single Image. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Alldieck_Tex2Shape_Detailed_Full_Human_Body_Geometry_From_a_Single_Image_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Alldieck_Tex2Shape_Detailed_Full_ICCV_2019_supplemental.pdf) [\[Code\\]](https://github.com/thmoa/tex2shape)
_Thiemo Alldieck, Gerard Pons-Moll, Christian Theobalt, Marcus Magnor_
##### PIFu: Pixel-Aligned Implicit Function for High-Resolution Clothed Human Digitization.[\[Project Page\]](https://shunsukesaito.github.io/PIFu/) [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Saito_PIFu_Pixel-Aligned_Implicit_Function_for_High-Resolution_Clothed_Human_Digitization_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Saito_PIFu_Pixel-Aligned_Implicit_ICCV_2019_supplemental.pdf)
_Shunsuke Saito, Zeng Huang, Ryota Natsume, Shigeo Morishima, Angjoo Kanazawa, Hao Li_
##### Monocular 3D Human Pose Estimation by Generation and Ordinal Ranking. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Sharma_Monocular_3D_Human_Pose_Estimation_by_Generation_and_Ordinal_Ranking_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Sharma_Monocular_3D_Human_ICCV_2019_supplemental.pdf) [\[Code\\]](https://github.com/ssfootball04/generative_pose)
_Saurabh Sharma, Pavan Teja Varigonda, Prashast Bindal, Abhishek Sharma, Arjun Jain_
##### HEMlets Pose: Learning Part-Centric Heatmap Triplets for Accurate 3D Human Pose Estimation. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Zhou_HEMlets_Pose_Learning_Part-Centric_Heatmap_Triplets_for_Accurate_3D_Human_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Zhou_HEMlets_Pose_Learning_ICCV_2019_supplemental.zip)
_Kun Zhou, Xiaoguang Han, Nianjuan Jiang, Kui Jia, Jiangbo Lu_
##### Single-Stage Multi-Person Pose Machines. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Nie_Single-Stage_Multi-Person_Pose_Machines_ICCV_2019_paper.pdf) [\[Code\\]](https://github.com/murdockhou/Single-Stage-Multi-person-Pose-Machines)
_Xuecheng Nie, Jiashi Feng, Jianfeng Zhang, Shuicheng Yan_
##### Single-Network Whole-Body Pose Estimation. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Hidalgo_Single-Network_Whole-Body_Pose_Estimation_ICCV_2019_paper.pdf) [\[Code\\]](https://github.com/CMU-Perceptual-Computing-Lab/openpose)
_Gines Hidalgo, Yaadhav Raaj, Haroon Idrees, Donglai Xiang, Hanbyul Joo, Tomas Simon, Yaser Sheikh_
##### Occlusion-Aware Networks for 3D Human Pose Estimation in Video.[\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Cheng_Occlusion-Aware_Networks_for_3D_Human_Pose_Estimation_in_Video_ICCV_2019_paper.pdf) [\[Supp\]](http://openaccess.thecvf.com/content_ICCV_2019/supplemental/Cheng_Occlusion-Aware_Networks_for_ICCV_2019_supplemental.pdf)
_Yu Cheng, Bo Yang, Bo Wang, Wending Yan, Robby T. Tan_

##### Ego-Pose Estimation and Forecasting As Real-Time PD Control.[\[Project Page\]](https://www.ye-yuan.com/ego-pose/) [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Yuan_Ego-Pose_Estimation_and_Forecasting_As_Real-Time_PD_Control_ICCV_2019_paper.pdf) [\[Code\\]](https://github.com/Khrylx/EgoPose)
_Ye Yuan, Kris Kitani_
##### End-to-end Learning for Graph Decomposition. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Song_End-to-End_Learning_for_Graph_Decomposition_ICCV_2019_paper.pdf)
_Jie Song, Bjoern Andres, Michael J. Black, Otmar Hilliges, Siyu Tang_
##### Through-Wall Human Mesh Recovery Using Radio Signals.[\[Project Page\]](http://rfavatar.csail.mit.edu/) [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Zhao_Through-Wall_Human_Mesh_Recovery_Using_Radio_Signals_ICCV_2019_paper.pdf) 
_Mingmin Zhao, Yingcheng Liu, Aniruddh Raghu, Tianhong Li, Hang Zhao, Antonio Torralba, Dina Katabi_
##### Camera Distance-Aware Top-Down Approach for 3D Multi-Person Pose Estimation From a Single RGB Image. [\[PDF\]](https://arxiv.org/abs/1907.11346) [\[Code\\]](https://github.com/mks0601/3DMPPE_ROOTNET_RELEASE)
_Gyeongsik Moon, Ju Yong Chang, Kyoung Mu Lee_
##### Deep Head Pose Estimation Using Synthetic Images and Partial Adversarial Domain Adaption for Continuous Label Spaces. [\[PDF\]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Kuhnke_Deep_Head_Pose_Estimation_Using_Synthetic_Images_and_Partial_Adversarial_ICCV_2019_paper.pdf) 
_Felix Kuhnke, Jorn Ostermann_

### 2019 CVPR
##### Deep High-Resolution Representation Learning for Human Pose Estimation. [\[PDF\]](https://arxiv.org/pdf/1902.09212.pdf) [\[Code\]](https://github.com/leoxiaobin/deep-high-resolution-net.pytorch)
_Ke Sun, Bin Xiao, Dong Liu, [Jingdong Wang](https://jingdongwang2017.github.io/index.html)_
##### 3D human pose estimation in video with temporal convolutions and semi-supervised training. [\[Project Cite\]](https://dariopavllo.github.io/VideoPose3D/) [\[PDF\]](https://arxiv.org/pdf/1811.11742.pdf) [\[Code\]](https://github.com/facebookresearch/VideoPose3D)
_Dario Pavllo, Christoph Feichtenhofer, David Grangier, Michael Auli_
##### Learning Regularity in Skeleton Trajectories for Anomaly Detection in Videos. [\[PDF\]](https://arxiv.org/pdf/1903.03295.pdf)
_Romero Morais, Vuong Le, Truyen Tran, Budhaditya Saha, Moussa Mansour, Svetha Venkatesh_
##### PoseFix: Model-agnostic General Human Pose Refinement Network. [\[PDF\]](https://arxiv.org/pdf/1812.03595.pdf) [\[Code\]](https://github.com/mks0601/PoseFix_RELEASE)
_Gyeongsik Moon, Ju Yong Chang, Kyoung Mu Lee_
##### Dense Intrinsic Appearance Flow for Human Pose Transfer. [\[PDF\]](https://arxiv.org/pdf/1903.11326.pdf) [\[Code\]](http://mmlab.ie.cuhk.edu.hk/projects/pose-transfer/)
_Yining Li, Chen Huang, Chen Change Loy_
##### Putting Humans in a Scene: Learning Affordance in 3D Indoor Environments. [\[Project Cite\]](https://sites.google.com/view/3d-affordance-cvpr19) [\[PDF\]](https://arxiv.org/pdf/1903.05690.pdf)
_Xueting Li, Sifei Liu, Kihwan Kim, Xiaolong Wang, Ming-Hsuan Yang, Jan Kautz_
##### Learning 3D Human Dynamics from Video. [\[Project Cite\]](https://akanazawa.github.io/human_dynamics/) [\[PDF\]](https://arxiv.org/pdf/1812.01601.pdf)
_Angjoo Kanazawa, Jason Y. Zhang, Panna Felsen, Jitendra Malik_
##### RepNet: Weakly Supervised Training of an Adversarial Reprojection Network for 3D Human Pose Estimation. [\[PDF\]](https://arxiv.org/pdf/1902.09868.pdf)
_Bastian Wandt, Bodo Rosenhahn_
##### Self-Supervised Learning of 3D Human Pose using Multi-view Geometry. [\[PDF\]](https://arxiv.org/pdf/1903.02330.pdf) [\[Code\]](https://github.com/mkocabas/EpipolarPose)
_Muhammed Kocabas, Salih Karagoz, Emre Akbas_
##### Fast and Robust Multi-Person 3D Pose Estimation from Multiple Views. [\[Project Cite\]](https://zju3dv.github.io/mvpose/) [\[PDF\]](https://arxiv.org/pdf/1901.04111.pdf) [\[Code\]](https://github.com/zju3dv/mvpose)
_Junting Dong, Wen Jiang, Qixing Huang, Hujun Bao, Xiaowei Zhou_
##### PifPaf: Composite Fields for Human Pose Estimation. [\[PDF\]](https://arxiv.org/pdf/1903.06593.pdf) [\[Code\]]()
_Sven Kreiss, Lorenzo Bertoni, Alexandre Alahi_
##### Weakly-Supervised Discovery of Geometry-Aware Representation for 3D Human Pose Estimation. [\[PDF\]](https://arxiv.org/pdf/1903.08839.pdf) [\[Code\]]() *(Oral)*
_Xipeng Chen, Kwan-Yee Lin, Wentao Liu, Chen Qian, Xiaogang Wang, Liang Lin_
##### CrowdPose: Efficient Crowded Scenes Pose Estimation and A New Benchmark. [\[PDF\]](https://arxiv.org/pdf/1812.00324.pdf) [\[Code\]](https://github.com/Jeff-sjtu/CrowdPose)
_Jiefeng Li, Can Wang, Hao Zhu, Yihuan Mao, Hao-Shu Fang, Cewu Lu_

### 2019 Others
##### \[2019 WACV\]Unsupervised Feature Learning of Human Actions as Trajectories in Pose Embedding Manifold. [\[PDF\]](https://arxiv.org/pdf/1812.02592.pdf)
_Jogendra Nath Kundu, Maharshi Gor, Phani Krishna Uppala, R. Venkatesh Babu_

### 2018 ECCV

##### Simple Baselines for Human Pose Estimation and Tracking. [\[PDF\]](https://arxiv.org/pdf/1804.06208.pdf) [\[Code\]](https://github.com/Microsoft/human-pose-estimation.pytorch)
_Bin Xiao, Haiping Wu, Yichen Wei_

##### Skeleton-Based Action Recognition with Spatial Reasoning and Temporal Stack Learning. [\[PDF\]](http://172.16.24.181/openaccess.thecvf.com/content_ECCV_2018/papers/Chenyang_Si_Skeleton-Based_Action_Recognition_ECCV_2018_paper.pdf) 
_Chenyang Si, Ya Jing, Wei Wang, Liang Wang, Tieniu Tan_
##### Deformable Pose Traversal Convolution for 3D Action and Gesture Recognition. [\[PDF\]](http://172.16.24.186/openaccess.thecvf.com/content_ECCV_2018/papers/Junwu_Weng_Deformable_Pose_Traversal_ECCV_2018_paper.pdf) 
_Junwu Weng, Mengyuan Liu, Xudong Jiang, Junsong Yuan_
##### Learning Human-Object Interactions by Graph Parsing Neural Networks. [\[PDF\]](http://172.16.24.175/openaccess.thecvf.com/content_ECCV_2018/papers/Siyuan_Qi_Learning_Human-Object_Interactions_ECCV_2018_paper.pdf) 
_Siyuan Qi, Wenguan Wang, Baoxiong Jia, Jianbing Shen, Song-Chun Zhu_


### 2018 CVPR
##### End-to-end Recovery of Human Shape and Pose.  [\[Project Cite\]](https://akanazawa.github.io/hmr/) [\[PDF\]](https://arxiv.org/pdf/1712.06584.pdf) [\[Code\]](https://github.com/akanazawa/hmr)
_Angjoo Kanazawa, Michael J. Black, David W. Jacobs, Jitendra Malik_


### 2018 Others

### 2017 ICCV
##### Towards 3D Human Pose Estimation in the Wild: a Weakly-supervised Approach. [\[PDF\]](https://arxiv.org/abs/1704.02447) [\[Code\]](https://github.com/xingyizhou/pose-hg-3d)
_Xingyi Zhou, Qixing Huang, Xiao Sun, Xiangyang Xue, Yichen Wei_
### 2017 CVPR

## Theses

## Other Related Papers

## Datasets
### 2D
- [MPII Human Pose Dataset](http://human-pose.mpi-inf.mpg.de/)
- [LSP](http://sam.johnson.io/research/lsp.html)
- [FLIC](https://bensapp.github.io/flic-dataset.html)
- [FLIC-plus](https://cims.nyu.edu/~tompson/flic_plus.htm)

### 3D
- [Human3.6M](http://vision.imar.ro/human3.6m/description.php)
- [HumanEva](http://humaneva.is.tue.mpg.de/)
- [MPI-INF-3DHP](http://gvv.mpi-inf.mpg.de/3dhp-dataset/)
- [Unite The People](http://files.is.tuebingen.mpg.de/classner/up/)

## Popular implementations

### PyTorch
- [pytorch-pose-hg-3d](https://github.com/xingyizhou/Pytorch-pose-hg-3d)
- [3d_pose_baseline_pytorch](https://github.com/weigq/3d_pose_baseline_pytorch)
- [pytorch_Realtime_Multi-Person_Pose_Estimation](https://github.com/tensorboy/pytorch_Realtime_Multi-Person_Pose_Estimation)
- [AlphaPose](https://github.com/MVIG-SJTU/AlphaPose/tree/pytorch)
- [pytorch-pose](https://github.com/bearpaw/pytorch-pose)
- [human-pose-estimation.pytorch](https://github.com/Microsoft/human-pose-estimation.pytorch)

### TensorFlow
- [tf-pose-estimation](https://github.com/ildoonet/tf-pose-estimation)
- [pose-tensorflow](https://github.com/eldar/pose-tensorflow)

### Torch
- [pose-hg-train](https://github.com/umich-vl/pose-hg-train)
- [pose-hg-demo](https://github.com/umich-vl/pose-hg-demo)

### Others
- [openpose](https://github.com/CMU-Perceptual-Computing-Lab/openpose)
- [DensePose](https://github.com/facebookresearch/DensePose)
