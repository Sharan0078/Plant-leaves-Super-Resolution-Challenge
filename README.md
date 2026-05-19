# Plant-leaves-Super-Resolution-Challenge

This project focuses on reconstructing high-resolution crop leaf images from heavily degraded low-resolution inputs using a Conditional Generative Adversarial Network (cGAN).

In real agricultural environments, images captured by drones and low-cost field sensors are often affected by compression artifacts, transmission noise, and hardware limitations. As a result, important biological details such as leaf veins, chlorosis patterns, and necrotic lesions become difficult to detect. The objective of this project is to restore those missing details by transforming distorted 32×32 images into high-quality 128×128 outputs.

The implemented model is based on a Conditional GAN architecture consisting of:

- **Generator:** Learns to denoise and upscale low-resolution images while preserving structural information.
- **Discriminator:** Distinguishes generated images from real high-resolution images and helps improve texture realism.

The entire network was trained completely from scratch without using pretrained models or external datasets, following the strict competition constraints.

The training pipeline combines reconstruction and adversarial losses to balance pixel-level accuracy with visual quality. Since the competition leaderboard evaluates predictions using Mean Absolute Error (MAE), the model emphasizes spatial accuracy and faithful reconstruction rather than generating unrealistic textures.

## Dataset
The dataset used for this project is not included in this repository due to its large size (several GBs).

Dataset Link:  
https://www.kaggle.com/competitions/plant-leaves-super-resolution-challenge/data

The dataset contains:
- Low-resolution degraded crop leaf images (32×32)
- High-resolution ground-truth images (128×128)

Please download the dataset from the Kaggle competition page before training or running the notebook.

## Key Features
- Blind 4× super-resolution
- Simultaneous denoising and upscaling
- GAN-based image reconstruction
- High-frequency biological texture recovery
- MAE-focused optimization
- Fully trained from scratch

## Technologies Used
- Python
- PyTorch
- NumPy
- OpenCV
- Matplotlib
- Kaggle Notebooks

## Evaluation
The final model is evaluated using Mean Absolute Error (MAE) between generated images and hidden ground-truth images.

## Applications
- Crop disease monitoring
- Smart agriculture systems
- Drone-based field analysis
- Agricultural image enhancement
- AI-assisted plant health diagnostics

This project demonstrates how deep learning and GAN-based super-resolution techniques can improve agricultural imaging systems operating under low-quality and bandwidth-constrained conditions.
