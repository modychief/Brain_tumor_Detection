# Brain Tumor Detection

This project aims to detect brain tumors in MRI scans using a custom Convolutional Neural Network (CNN) model. The model is trained on a dataset of MRI scans of the brain.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Results](#results)

## Introduction

Brain tumors are abnormal growths of cells in the brain that can cause various neurological symptoms and potentially be life-threatening. Early detection of brain tumors is crucial for timely intervention and improved patient outcomes. This project focuses on developing an automated system to detect brain tumors from MRI scans, aiding medical professionals in their diagnosis.

## Dataset

The dataset used in this project consists of MRI scans of the brain, with labeled images indicating the presence or absence of tumors.
The dataset can be obtained from https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection 
Some samples of the dataset are :
Class "No"
![image](https://github.com/modychief/Brain_tumor_Detection/assets/112490642/3c39f050-4ff4-4de5-a9fc-d3d32742479c)

Class "Yes"
![image](https://github.com/modychief/Brain_tumor_Detection/assets/112490642/221c7a52-1549-47b2-a52a-933afc63a69a)

## Model Architecture
We made a custom model to train the data which is as follows:
1. **Input Layer**: The first layer of the model specifies the input shape for the images. In this case, the input shape is (224, 224, 3), indicating RGB images with a resolution of 224x224 pixels.

2. **Convolutional Layers**:
   - Conv2D Layer 1: It has 16 filters and a kernel size of (3, 3). The ReLU activation function is applied to introduce non-linearity.
   - Conv2D Layer 2: It has 36 filters and a kernel size of (3, 3). The ReLU activation function is applied.
   - MaxPooling2D Layer 1: It performs max pooling with a pool size of (2, 2), reducing the spatial dimensions by half.
   - Conv2D Layer 3: It has 64 filters and a kernel size of (3, 3). The ReLU activation function is applied.
   - MaxPooling2D Layer 2: It performs max pooling with a pool size of (2, 2).
   - Conv2D Layer 4: It has 128 filters and a kernel size of (3, 3). The ReLU activation function is applied.
   - MaxPooling2D Layer 3: It performs max pooling with a pool size of (2, 2).

3. **Dropout Layer**:
   - Dropout Layer: It applies dropout regularization with a rate of 0.25, randomly setting a fraction of input units to 0 during training to prevent overfitting.

4. **Flatten Layer**:
   - Flatten Layer: It converts the 3D feature maps into a 1D feature vector, preparing the data for the fully connected layers.

5. **Fully Connected Layers**:
   - Dense Layer 1: It has 64 units and applies the ReLU activation function.
   - Dropout Layer: Another dropout layer with a rate of 0.25 is added.
   - Dense Layer 2: It has 1 unit and applies the sigmoid activation function. This final layer produces a single output representing the probability of a brain tumor being present (binary classification).
  ![image](https://github.com/modychief/Brain_tumor_Detection/assets/112490642/1d570812-2e40-42d7-980a-0138c5a41284)


This model architecture consists of convolutional layers for feature extraction, pooling layers for downsampling, dropout layers for regularization, and fully connected layers for classification. It aims to learn discriminative features from the input MRI scans and detect the presence of brain tumors.

## Results
We got the accuracy of <span style="color:blue">0.9756</span>, 
and the loss is <span style="color:blue">0.1109</span>
![image](https://github.com/modychief/Brain_tumor_Detection/assets/112490642/ba65060a-57ee-41ed-8dd2-3b6c3030121c)

Our Loss chart
![image](https://github.com/modychief/Brain_tumor_Detection/assets/112490642/fe4c4eff-8d04-4370-bbc3-83ac1d8458d1)

And Our Accuracy Chart is
![image](https://github.com/modychief/Brain_tumor_Detection/assets/112490642/a2a6aa38-6d1e-4f46-ac97-bc9c603146b6)




