# Lacuna Malaria Detection Dataset Using CNNs

## Overview

This project aims to develop a Convolutional Neural Network (CNN) to classify and predict bounding box coordinates for microscopic blood sample images. The dataset consists of labeled images, each containing a malaria parasite stage (Trophozoite), white blood cells (WBC), or negative for malaria (NEG). The task involves both classification and regression:

- **Classification**: Classify each image into one of three classes:
  - **NEG** (Negative for Malaria)
  - **Trophozoite** (Malaria parasite stage)
  - **WBC** (White Blood Cells)
  
- **Regression**: Predict the bounding box coordinates (`xmin`, `xmax`, `ymin`, `ymax`) for each object in the image.

## Dataset Details

- **Image Content**: The dataset contains microscopic images of blood samples.
- **Labeling**: Each image is labeled with:
  - A class label: `NEG`, `Trophozoite`, or `WBC`.
  - Bounding box coordinates: `xmin`, `xmax`, `ymin`, `ymax` representing the object of interest in the image.
  
- **Data Split**: The dataset must be split into three sets:
  - Training set
  - Validation set
  - Test set

## CNN Model Requirements

### Implementation from Scratch

No pre-trained models are allowed. You will need to design and implement the architecture of your CNN to handle both classification and regression tasks. This includes:

- Designing layers for feature extraction.
- Combining layers for classification and bounding box regression.

### Data Augmentation

To improve model robustness and generalization, apply the following data augmentation techniques:

- **Rotation**: Rotate images to introduce orientation invariance.
- **Scaling and Zooming**: Change the scale of objects in the images.
- **Flipping**: Use horizontal and vertical flipping for increased data diversity.
- **Random Cropping**: Crop random regions of the image to improve spatial awareness.
- **Brightness/Contrast Adjustment**: Alter image brightness and contrast for different lighting simulations.
- **Gaussian Noise**: Add noise to the images to prevent overfitting and improve model generalization.

> **Note**: For transformations like rotations and cropping, ensure that the bounding box coordinates (`xmin`, `xmax`, `ymin`, `ymax`) are adjusted accordingly.

### Model Design and Hyperparameter Tuning

Experiment with the architecture and hyperparameters of your CNN, such as:

- **Fully Connected Layers**: Number of neurons.
- **Convolutional Layers**: Number of layers and filter sizes.
- **Activation Functions**: ReLU, LeakyReLU, etc.
- **Optimization Algorithms**: Adam, SGD, etc.
- **Loss Functions**:
  - **Classification task**: Categorical Cross-Entropy.
  - **Regression task**: Mean Squared Error (MSE) or Smooth L1 Loss for bounding box prediction.

## Exploratory Data Analysis (EDA)

Before training, perform an analysis of the dataset. Key areas to explore include:

- **Class Distribution**: Visualize the distribution of images across the three classes.
- **Bounding Box Distribution**: Analyze the size and location of bounding boxes in the images.
- **Image Quality**: Examine variations in brightness, contrast, and noise levels.
- **Image Resolutions**: Verify the uniformity of image size and quality.

This analysis will guide your preprocessing steps and help in understanding the dataset better.

## Deliverables

Submit the following:

1. **Code File (.ipynb)**: A Jupyter notebook containing your code for data analysis, model building, training, and evaluation.
2. **Scientific Report**: A detailed report covering:
   - Dataset and preprocessing steps.
   - CNN architecture, including explanations of layer choices and hyperparameter tuning.
   - Insights and findings from your EDA.
   - Results, including classification accuracy and bounding box prediction accuracy.
3. **Theoretical Questions**: Responses to a set of theoretical questions related to deep learning, CNNs, data augmentation, and object detection.

## Evaluation Criteria

Your work will be evaluated based on the following:

- **Model Performance**: Accuracy in both classification and bounding box prediction on the test set.
- **Data Augmentation and Preprocessing**: The use and justification of data augmentation techniques.
- **Model Architecture and Tuning**: Creativity and thoroughness in adjusting the CNN architecture.
- **Scientific Reporting**: Clarity and depth in reporting, including hyperparameter tuning, model performance, and insights learned during the project.

This project provides an opportunity to apply your skills in both CNN design and object detection, focusing on a practical, real-world application in malaria detection.
