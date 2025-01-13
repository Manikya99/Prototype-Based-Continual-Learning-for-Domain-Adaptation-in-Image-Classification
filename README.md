# Prototype-Based-Continual-Learning-for-Domain-Adaptation-in-Image-Classification

This project explores the application of Learning with Prototypes (LwP) for continual learning and domain adaptation, with a focus on image classification tasks using the CIFAR-10 dataset.

## Project Overview

### Objectives
- Implement a prototype-based model to perform continual learning with both homogeneous and heterogeneous input distributions.
- Maintain model performance on newly added datasets while avoiding catastrophic forgetting of prior datasets.
- Leverage Vision Transformer (ViT) for feature extraction, enhancing representation quality for classification tasks.

### Key Tasks
1. **Continual Learning with Homogeneous Input Distributions**
   - Developed a sequential learning framework to update the model iteratively across datasets (D1 to D10).
   - Ensured high accuracy on both new and previously evaluated datasets.

2. **Continual Learning with Heterogeneous Input Distributions**
   - Extended the framework to handle datasets (D11 to D20) with distinct input distributions.
   - Employed confidence-based filtering and memory buffering to retain performance on earlier datasets.

## Methodology

### Feature Extraction
- **Vision Transformer (ViT)**:
  - Used the `vit-base-patch16-224-in21k` pretrained model for feature extraction.
  - Applied resizing and normalization to preprocess images.
  - Extracted global feature vectors using mean pooling on the last hidden state.

### Sequential Learning
- **Task 1**:
  - Computed class means for labeled datasets to initialize the model.
  - Updated class means iteratively using pseudo-labeled data for subsequent datasets.

- **Task 2**:
  - Adapted the model to heterogeneous distributions with an exponential moving average for class means.
  - Maintained a memory buffer to store representative samples, mitigating catastrophic forgetting.

## Results
- Achieved robust continual learning performance on CIFAR-10 datasets, as evidenced by accuracy matrices for both tasks.
- Effectively adapted to evolving data distributions while preserving knowledge from earlier datasets.

