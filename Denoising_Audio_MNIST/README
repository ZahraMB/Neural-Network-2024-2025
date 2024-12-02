# Audio Denoising with Autoencoders

This project focuses on designing and training an autoencoder to denoise audio samples from the **Audio MNIST** dataset. The goal is to enhance the quality of noisy audio files, making them more usable for downstream applications.

## Objective

- **Denoising Task**: Convert noisy audio samples into clean ones using autoencoders.
- **Dataset**: Audio MNIST, comprising 30,000 clean and noisy audio samples of spoken digits (0-9) recorded by 60 speakers.
- **Link**: [Audio MNIST](https://www.kaggle.com/datasets/mahdiahmadi81/noisy-audio-mnist).
## Dataset Overview

The **Audio MNIST** dataset includes:
- **Clean Audio**: 30,000 samples of digits spoken by 60 speakers.
- **Noisy Audio**: Corresponding 30,000 samples with a Signal-to-Noise Ratio (SNR) of -8 dB.
- **Metadata**: Speaker information (age, gender) provided in `audioMNIST_meta.txt`.

## Feature Extraction and Preprocessing

### Feature Extraction
- Spectrograms generated using Short-Time Fourier Transform (STFT) serve as model inputs (noisy) and targets (clean).
- STFT parameters: FFT size of 2048.

### Preprocessing
- Audio files standardized to 1 second by trimming or padding.
- Resampling to a uniform sample rate of 22,050 Hz.

### Augmentation
- **Gaussian and Pink Noise** added to create an augmented dataset of 3,000 samples.
- Augmentation improves model robustness to various noise conditions.

## Model Implementation

An autoencoder architecture was developed to:
1. Train on noisy spectrograms to reconstruct clean versions.
2. Evaluate performance based on Signal-to-Noise Ratio (SNR) improvement.

## Results

### Model Performance
- Average SNR improvement: **0.52 dB** on the test set.

### Performance Analysis
- **Across Speakers and Digits**: Bar plots show SNR improvement for each category.
- **Speaker Attributes**: SNR improvement analyzed by age, gender, and accent, revealing attribute-specific insights.

## Key Contributions

- Augmented dataset for robust training.
- Quantitative analysis of denoising performance using SNR metrics.
- Exploration of speaker-specific and digit-specific performance variations.

## Report
The detailed report of this project is provided in Practical Report.pdf
