# 《Feature Mapping for Learning Fast and Accurate 3D Pose Inference》
* Authors: Mahdi Rad, Markus Oberweger, Vincent Lepetit, CVPR, 2018
* Keywords: Synthetic images to guide learning

## Contributions:
- Propose a simple and efficient method for exploiting synthetic images when training a Deep Network to predict a 3D pose from an image: given a real image of the target object, firstly compute the features for the image, map them to the feature space of synthetic images, and finally use the resulting features as input to another network which predicts the 3D pose.
- Show that network trained effectively by using synthetic images performs very well in practice, and inference is faster and more accurate than with an exemplar-based approach.
## Proposed Approach:
- Goal: exploit synthetic images to guide learning, when training a Deep Network to predict a 3D pose from a real image.
- Model Architecture:
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/42.png)
- Training
    * Train a feature extractor and 3D pose predictor by synthetic images.
    * Mapping Network
	    * Trained to map features of the real images into the synthetic feature space;
	    * Trained using pairs of images, each pair is made of one of the available real images and of one synthetic image of the target object rendered under the same 3D pose as in the real image;
	    * Minimize the distance between the features extracted from the synthetic images and the features extracted from the real image during training.
- Effect of the Learned Mapping
    * For each pair, only a few feature coefficients are responsible for the domain gap, and they can be attenuated by the mapping.
    * ![](https://github.com/TerenceCYJ/3D_Pose_Papers/blob/master/Images/43.png)
- Network Details
    * Use two Residual blocks for mapping network to map feature vectors of size 1024;
    * The network architectures of feature extractor and pose predictor depend on the application.
	    * For 3D object pose estimation from color images: use VGG-16 network for initializing feature extractor(10 convolutional layers) and 2 fully-connected layers with 1024 neurons, and for pose predictor use a single fully-connected layer with 16 outputs(2 coordinates for each corner of the bounding box).
	    * For 3D hand pose estimation from depth maps: for feature extractor similar to the 50-layer Residual Network with 4 residual modules, remove the Global Average Pooling, add two fully-connected layers with 1024 neurons each; use a single fully-connected layer with 42 outputs(3 for each of the 14 joints) for the pose prediction network.
## Experiment:
- 3D Object Pose Estimation
    * raining set creation: generate in total 5M synthetic training images online during training, from poses randomly sampled on the upper hemisphere of the object;
    * Using our method systematically improves the results compared to using only real images for training.
- 3D Hand Pose Estimation
    * Training set creation: use 5M synthetic images of the handthat are rendered online during training from poses of thetraining set perturbed with randomly added articulations; synthetic depth maps do not contain any noise;
## Strengths / Novelties：
- Presented an approach that learns a mapping between the two domains from synthetic images rendered under the same pose as the available real training images, jointly with feature extraction and pose inference.
