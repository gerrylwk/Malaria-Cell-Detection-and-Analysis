# Malaria-Cell-Detection-and-Analysis
Investigation of traditional ML models and CNNs on Malaria Cell Detection


This project aims to investigate the difference between traditional ML methods such as Logistic Regression(LR) and Perceptron Learning Algorithm(PLA) vs new ML methods(Convolutional Neural Networks), as well as investigating where each model failed to classify the images correctly. For the CNN model, we have chosen to use variations of VGG-16 to experiment on. Dataset obtained from https://www.kaggle.com/iarunava/cell-images-for-detecting-malaria 

We first have a baseline model for the 3 methods:
1) LR
2) PLA
3) CNN

We then move on to perform experiments on CNN to try and further improve its accuracy as well as False Negative Rate(FNR).
Experiments include:
1) Hyperparameter selection using Hyperas
2) Effect of Weighted penalties for false negatives
3) Effect of different layers 
4) Effect of Optimisers
5) Transfer learning using pre-trained VGG-16

We then created a finalised model, a variant of the VGG-16 and tested it with the 3 base models from above. 
Images that were wrongly classified were printed so that we have a better idea of what kind of images did the model fail to predict.

Conclusion:
CNN is able to achieve extremely high accuracy and low FNR, provided that the images are noiseless. The malaria cell dataset contained some images that seem to be in the wrong class, however, provenance of data states that the images were laballed by a specialist in a reknowned institution, thus human error might be at play here. Or else, malaria cells cannot be visually detected. 

Contributors: Lee Siying, Dylan Tan Cheng Song, Jennifer Chessa, Samuel Kristianto Tjong, Teo Zhi Yu Dawn

Full Notebook Structure:
1) Preprocessing and Augmentation

	Here we read in the images from the folders into arrays, as well as perform image augmentation by adding 2 randomly rotated images on top of each image.
2) Load the training and test arrays
3) Train Test Split

	Standardise training,validation and test set for all models
4) Base Model

	-Perceptron Learning Algorithm(PLA)
	
	-Logistic Regression
	
	-Simplified VGG-16(Base)
	
5) Hyperas 

	This section takes very long to run
6) Experiments on Optimisers

	6 different optimisers and a plot
7) Effect of weights on FNR

	Experimenting on different weights to assign to false negatives
8) Effect of number of VGG-16 layers

	Testing different number of layers for accuracy. Tested 7,12,16 layer model
9) Transfer Learning with pre-trained VGG-16

	Tested with a pre-trained VGG-16 on the malaria cell dataset
10) Final Modified VGG-16 and Base model

	Final model to use with weighted penalties, and comparing the results to the base model
11) Identifying False Negatives and False Positives

	Here we plot out the images that were misclassified for PLA, Logistic Regression and the final model
