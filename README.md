# Image Preprocessing Pipeline – Assignment

## Overview
This project demonstrates a custom image preprocessing pipeline using a publicly available color image dataset.  
The main goal is to apply multiple preprocessing transformations to images and analyze how each step affects the image shape and pixel values.

The **CIFAR-10 dataset** is used, and **two color images** are selected for processing.

---

## Dataset Used
- **Name:** CIFAR-10
- **Type:** Color images (RGB)
- **Image Size:** 32 × 32
- **Source:** torchvision.datasets.CIFAR10

Two images are taken from the test dataset for demonstration.

---

## Preprocessing Pipeline Steps

The following preprocessing steps are applied **one by one** to both images:

### 1. Resize
- Original image size is resized from **32 × 32** to **64 × 64**
- This helps standardize the image size for neural networks

### 2. Grayscale Conversion
- Converts RGB images into **single-channel grayscale**
- Reduces complexity and focuses on intensity information

### 3. Rotation
- Images are rotated by **30 degrees**
- Helps improve model robustness to orientation changes

### 4. Horizontal Flip
- Images are flipped horizontally
- Common data augmentation technique

### 5. Tensor Conversion and Normalization
- Images are converted into PyTorch tensors
- Pixel values are normalized to the range **[-1, 1]**
- Makes training faster and more stable

---

## Bonus: Custom Sharpening Filter
A **custom sharpening kernel** is applied to the images:
- Enhances edges and fine details
- Increases contrast around object boundaries
- Pixel values may slightly increase due to edge enhancement

---

## Visualization
- Each preprocessing step is visualized
- Images are displayed **side-by-side**
- Image **shape and pixel value range** are printed after each step

---

## Final Output Tensor
After preprocessing:
- The two images are combined into a single batch tensor
- Tensor shape:

