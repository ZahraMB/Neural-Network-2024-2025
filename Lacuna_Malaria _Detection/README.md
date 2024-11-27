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
- **Random Cropping**: Crop random regions of the image to improve spatial 
