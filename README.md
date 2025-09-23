# Pest Image Classification (CNN → VGG16 Transfer Learning)

## Introduction
This project tackles a **multiclass image classification problem** in agriculture: identifying common crop pests from images.  
Pests are a major threat to food security — they reduce farmer productivity, damage crops, and contribute to significant economic losses worldwide.  

The dataset comes from Kaggle: [Pest Data](https://www.kaggle.com/datasets/simranvolunesia/pest-dataset/data), which contains images of 9 pest categories.  
By applying deep learning techniques, this project demonstrates how early pest detection can be supported with machine learning, potentially helping farmers and agricultural researchers.


## TL;DR
- **Task:** Pest recognition from images (9 classes)  
- **Dataset:** Kaggle Pest Data (link above)  
- **Models:** Custom CNN → VGG16 (transfer learning)  
- **Best Val Acc:** **98%** (CNN baseline ~95%)  
- **Key Techniques:** Data augmentation, transfer learning  
- **Run in minutes:** Sample dataset included; full dataset fetchable with one command  

---


## Data

**Source:** Kaggle – [Pest Data](https://www.kaggle.com/datasets/simranvolunesia/pest-dataset/data)  
**Type:** Image classification dataset (multiclass, 9 categories)

### Dataset Description
- **Classes (9):** aphids, armyworm, beetle, bollworm, grasshopper, mites, mosquito, sawfly, stem borer.  
- **Split (balanced):**  
  - Training set: ~300 images per class
  - Test set: ~50 images per class

### Key Characteristics
- **Intra-class variation:** The same pest looks different depending on life stage (larvae vs adult), color, and angle  
- **Inter-class similarity:** Some pests (armyworm, bollworm, sawfly) look visually similar as larvae, making classification challenging  
- **Background diversity:** Images include natural field photos, lab setups, plain backgrounds, and noisy scenes  
- **Data quality:** Being web-scraped, there may be duplicates or occasional label noise → mitigated with data augmentation and careful train/test splits

### Representative Sample
The grid below illustrates several categories (stem borer, sawfly, armyworm, mosquito, aphids, beetle).  
Although it does not cover all nine classes, it highlights **dataset diversity** across pest types, life stages, and imaging conditions.

<p align="center">
  <img src="assets/pest_samples.png" width="600" />
</p>


---

## Approach & Models

### Baseline CNN
- Built a simple convolutional neural network from scratch.  
- Validation Accuracy: ~95.3%  
- Demonstrates capability to extract basic patterns but limited generalization.  

### VGG16 (Transfer Learning)
- Pretrained ImageNet weights, fine-tuned for pest dataset.  
- Validation Accuracy: **98%**  
- Robust feature extraction handles variation in pest life stages and backgrounds.  

### Data Augmentation
- Applied random rotations, flips, zoom, and brightness adjustments.  
- Improved robustness against lighting/background noise.  

### Model Results
<p align="center">
  <img src="assets/plots/train_curve.png" width="320" />
  <img src="assets/plots/confusion_matrix.png" width="320" />
  <img src="assets/plots/pred_grid.png" width="320" />
</p>

---

## Model Description and Accuracy

### Initial Model – Custom CNN
The project began with a **custom Convolutional Neural Network (CNN)** designed for pest image classification.  
Architecture: three convolutional layers with pooling, followed by fully connected layers.  
- **Training Accuracy:** ~96.6%  
- **Validation Accuracy:** ~95.3%  

This baseline established that the dataset was learnable, but the model struggled with generalization on visually similar pests.

### Transition to VGG16 (Transfer Learning)
To improve performance, the model was upgraded to **VGG16 with transfer learning**, leveraging pretrained ImageNet weights for stronger feature extraction.  
- **Training Accuracy:** ~100%  
- **Validation Accuracy:** ~98%  

This significantly improved robustness, particularly in handling pest variations across life stages, lighting, and backgrounds.

### Benchmark Comparison
For context, Kaggle notebooks using the same dataset typically report validation accuracy around **94%**.  
This project’s transfer learning model achieved **~98%**, demonstrating improved model design and training pipeline effectiveness.
