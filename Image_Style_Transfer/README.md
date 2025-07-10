# Landscape to Fauvism: Artistic Style Transfer Using CycleGAN

This project implements a CycleGAN-based neural network to transform landscape photographs into Fauvism-style paintings. By leveraging the visual richness of the WikiArt dataset and the expressive style of Fauvism, the model creates visually compelling, vibrant artistic renditions of real-world landscapes.

---

## Project Objective

The goal is to develop a model capable of applying the **Fauvism** artistic style to landscape images. Fauvism is known for its vivid colors and expressive brushwork, making it an ideal choice for turning natural scenes into emotionally resonant artworks.

The model takes a real landscape photo as input and outputs a stylized version that captures the color intensity, abstraction, and compositional harmony characteristic of Fauvism.

---

## Data Preparation and Preprocessing

### Datasets Used

- **Landscape photographs** (natural scenery)
- **WikiArt** subset filtered for Fauvism-style paintings

### Fauvism Style Selection

Fauvism was chosen for its ability to:

- Preserve structural elements while enhancing visual expressiveness
- Apply bold, saturated colors without losing the image’s coherence
- Emphasize artistic abstraction while maintaining recognizability

### Dataset Curation

- 923 Fauvism paintings extracted from WikiArt  
- 923 landscape images randomly selected to match the style set  
- This 1:1 balance was necessary to prevent memory overflow during training

---

## Model Architecture

This project uses the **CycleGAN** architecture, consisting of:

### Generator

- Two generators: Photo → Style and Style → Photo  
- Each generator includes:
  - Convolutional layers with downsampling  
  - Residual blocks to preserve features and gradients  
  - Upsampling layers to restore image dimensions  
  - Final convolution layer with Tanh activation

### Discriminator

- Two discriminators: one per domain (landscape and Fauvism)  
- Architecture:
  - Multiple convolutional layers with LeakyReLU  
  - Final output layer predicts the realism of the input image

---

## Loss Functions

- **Adversarial Loss**: Encourages generators to create realistic outputs  
- **Cycle Consistency Loss**: Ensures that converting an image and then converting it back results in the original image  
- **Identity Loss**: Helps preserve color and content when feeding target domain images into the generator

---

## Training Procedure

- Alternate training of generators and discriminators  
- Optimization using **Adam optimizer** with:
  - Learning rate: 0.0002  
  - β1 = 0.5, β2 = 0.999  
- Custom learning rate scheduler to decay the learning rate over time for smoother convergence  
- Model trained for 10 epochs on paired datasets

---

## Results and Evaluation

After 10 epochs of training:

- The model successfully transferred the Fauvism style to landscape images  
- Results were evaluated both qualitatively (visual inspection) and quantitatively  
- Stylized outputs demonstrated strong preservation of form with vibrant, expressive color transformations

---

## Report

For full details on implementation, architecture, loss functions, training procedure, and evaluation, please refer to:

**`report.pdf`**

---

