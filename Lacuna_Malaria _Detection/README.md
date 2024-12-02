# Lacuna Malaria Detection Dataset Using CNNs

## Overview

For this project, the goal is to build a Convolutional Neural Network (CNN) that can both classify and predict bounding boxes for images of blood samples. The dataset contains microscopic images labeled with three categories:

- **NEG**: Negative for malaria
- **Trophozoite**: Malaria parasite stage
- **WBC**: White Blood Cells

The task is not just to classify these images but also to predict the bounding box coordinates for each object (i.e., the parasite or white blood cells) in the image, making this a combination of both classification and regression.

## Dataset Details

- **Images**: The dataset contains labeled microscopic images of blood samples, where each image has:
  - A class label (NEG, Trophozoite, or WBC).
  - Bounding box coordinates (`xmin`, `xmax`, `ymin`, `ymax`) for the object of interest in the image.

- **Data Split**: You’ll need to split the dataset into three sets:
  - Training set
  - Validation set
  - Test set

## CNN Model Requirements

### No Pre-trained Models – Build from Scratch

For this project, you’ll be designing and building a CNN from scratch (no pre-trained models!). This means you’ll need to create the network architecture yourself, especially since the output is different from conventional CNN tasks.

- **Feature Extraction**: Design layers for extracting features from the images.
- **Combined Architecture**: Combine layers for both classification and bounding box regression in one network.

### Data Augmentation

To make your model more robust, apply various data augmentation techniques to your images. Here are some techniques you should try:

- **Rotation**: Rotate images to make the model less sensitive to orientation.
- **Scaling & Zooming**: Change the scale of the objects in the images.
- **Flipping**: Use horizontal and vertical flipping to diversify your data.
- **Random Cropping**: Randomly crop parts of the image to improve spatial awareness.
- **Brightness/Contrast Adjustment**: Vary brightness and contrast to simulate different lighting conditions.
- **Gaussian Noise**: Add noise to images to help prevent overfitting.

> **Note**: If you apply transformations like rotation or cropping, make sure to adjust the bounding box coordinates accordingly!

### Model Design and Hyperparameter Tuning

There’s a lot of freedom here to experiment with different architectures. Play around with:

- **Fully Connected Layers**: Try different numbers of neurons.
- **Convolutional Layers**: Experiment with the number of layers and filter sizes.
- **Activation Functions**: Test functions like ReLU and LeakyReLU.
- **Optimization Algorithms**: Try Adam, SGD, or others.
- **Loss Functions**:
  - **Classification task**: Use Categorical Cross-Entropy.
  - **Regression task**: Try Mean Squared Error (MSE) or Smooth L1 Loss for bounding box prediction.

## Exploratory Data Analysis (EDA)

Before jumping into training, take some time to explore the dataset. Some key things to look at include:

- **Class Distribution**: How are the images distributed across the three classes? Are they balanced?
- **Bounding Box Distribution**: What are the sizes and locations of the bounding boxes?
- **Image Quality**: Are there variations in brightness, contrast, or noise in the images?
- **Image Resolutions**: Are the images of uniform size and quality?

This will help guide your preprocessing choices and give you a better understanding of what you’re working with.


This project is an opportunity to apply your deep learning skills in a real-world task—detecting malaria from blood samples using CNNs and object detection.
