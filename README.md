# Malaria-Cell-Detection-and-Analysis
Investigation of traditional ML models and CNNs on Malaria Cell Detection


This project aims to investigate the difference between traditional ML methods such as Logistic Regression(LR) and Perceptron Learning Algorithm(PLA) vs new ML methods(Convolutional Neural Networks), as well as investigating where each model failed to classify the images correctly. For the CNN model, we have chosen to use variations of VGG-16 to experiment on.

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
