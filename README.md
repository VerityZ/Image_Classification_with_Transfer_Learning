### Image Classification with Transfer Learning

#### Project Overview
This repository focusing on applying custom convolutional neural network (CNN) model to the adoption of transfer learning with VGG16 for image classification.

#### Problem Statement
Pests are a huge threat! Farmers are hard at work however their productivity is reduced due to pests, so this dataset can be used to identify pests or maybe other use cases involving pest identification. 

#### Dataset Description
- Type of dataset: Image Dataset.
- training images: 300 images per pest.
- testing images: 50 images per pest.
- Data Source: Automatic script to scrape images of pest from Google through Selenium and Chrome Driver.
- Pests: aphids, armyworm, beetle, bollworm, grasshopper, mites, mosquito, sawfly, stem borer.

#### Model Description and Accuracy
###### Initial Model - Custom CNN
First, the project built a custom CNN architecture for the pest image classification task. The model consisted of three convolutional layers followed by pooling layers and fully connected layers.
- **Training Accuracy**: Reached to 96.59%.
- **Validation Accuracy**: Peaked around 95.33%.

###### Transition to VGG16 with Transfer Learning
Then, using the VGG16 model, to leverage its robust feature-extracting capabilities. This move was aimed at improving accuracy and reliability.
- **Training Accuracy**: Improved to a perfect 100%.
- **Validation Accuracy**: Increased to 98%.

#### Comparison with Kaggle Notebooks
On Kaggle, the best validation accuray currenlty is 94%. My model stands out by achieving better accuracy. 
