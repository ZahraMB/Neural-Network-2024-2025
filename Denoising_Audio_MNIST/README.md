# Audio Denoising with Autoencoders

This repository presents a deep learning project focused on denoising audio using autoencoders. The model is trained to enhance noisy audio signals from the **Audio MNIST** dataset, producing cleaner versions that improve usability in real-world speech processing tasks.

---

## Project Overview

### Objective

Design and train an autoencoder to transform noisy audio samples into clean ones. This denoising process aims to improve audio quality for applications such as speech recognition and acoustic analysis.

### Dataset

The project uses the **Audio MNIST** dataset, which contains:

- 30,000 clean audio samples of spoken digits (0–9)  
- 30,000 corresponding noisy audio samples with an SNR of -8 dB  
- Metadata (`audioMNIST_meta.txt`) detailing speaker attributes such as age and gender

This dataset offers paired clean-noisy audio samples ideal for supervised denoising.

---

## Model Architecture

The autoencoder operates on spectrograms of the audio and consists of:

- An **encoder** with three convolutional layers and batch normalization  
- A **decoder** with upsampling layers and convolutional reconstruction  
- **ReLU** activation in hidden layers and **Sigmoid** activation in the output layer

#### Training Configuration

- Optimizer: Adam  
- Learning rate: 0.0001  
- Loss function: Mean Squared Error (MSE)

---

## Performance

The model was evaluated on a separate test set using Signal-to-Noise Ratio (SNR) improvement.

- **Average SNR improvement**: +0.52 dB

Denoised outputs were compared with clean spectrograms to assess reconstruction quality.

---

## Speaker Attribute Analysis

The report includes a detailed analysis of how speaker and contextual characteristics influence denoising performance:

- **Accent** and **origin** significantly affected SNR improvement  
- **Gender** and **age** showed moderate influence  
- **Native speakers** showed slightly lower SNR improvement than non-native speakers

These findings emphasize the value of incorporating speaker diversity and contextual awareness into audio denoising systems.

---

## Report

All details of the implementation, model evaluation, and attribute analysis are available in:

**`Practical Report.pdf`**

---
