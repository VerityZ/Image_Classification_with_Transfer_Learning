### Math251 Take Home Exam 2 - Image Classification with Transfer Learning

#### Project Overview
This repository hosts the Take Home Exam for Math251, focusing on applying custom convolutional neural network (CNN) model to the adoption of transfer learning with VGG16 for image classification.

#### Problem Statement
Pests are a huge threat! Farmers are hard at work however their productivity is reduced due to pests, so this dataset can be used to identify pests or maybe other use cases involving pest identification. 

#### Dataset Description
a. Type of dataset: Image Dataset
b. No. of training images: 300 images per pest
c. No. of testing images: 50 images per pest
d. Data Source: Automatic script to scrape images of pest from Google through Selenium and Chrome Driver
e. Pests: aphids, armyworm, beetle, bollworm, grasshopper, mites, mosquito, sawfly, stem borer

#### Model Description

###### Initial Model - Custom CNN
First, the project built a custom CNN architecture for the pest image classification task. The model consisted of three convolutional layers followed by pooling layers and fully connected layers:
- **Convolutional Layers**: Aimed to extract meaningful features from the images.
- **Pooling Layers**: Reduced the dimensionality of the feature maps, thus reducing the number of parameters and computation in the network.
- **Fully Connected Layers**: Served as classifiers on the features extracted and pooled by the previous layers.

###### Transition to VGG16 with Transfer Learning
Then, using the VGG16 model, to leverage its robust feature-extracting capabilities. This move was aimed at improving accuracy and reliability.

#### Results Achieved

###### Initial Model Results
- **Training Accuracy**: Reached to 96.59%.
- **Validation Accuracy**: Peaked around 95.33%.

###### After Transitioning to VGG16
- **Training Accuracy**: Improved to a perfect 100%.
- **Validation Accuracy**: Increased to 98%.

#### Comparison with Kaggle Notebooks
On Kaggle, the best validation accuray currenlty is 94%. My model stands out by achieving better accuracy. 
