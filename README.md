# Anime Face Generator with GANs

## Project Overview

This project implements a Generative Adversarial Network (GAN) for generating anime face images. The GAN consists of a generator and a discriminator trained on the Anime Face Dataset sourced from Kaggle. The project is implemented in PyTorch and includes data loading, preprocessing, model creation, training, and visualization.

## Table of Contents

- [Dataset Acquisition](#dataset-acquisition)
- [Data Preprocessing](#data-preprocessing)
- [Data Visualization](#data-visualization)
- [Device Handling](#device-handling)
- [Model Architecture](#model-architecture)
- [Training the GAN](#training-the-gan)
- [Results and Visualization](#results-and-visualization)
- [Hyperparameters and Training Configuration](#hyperparameters-and-training-configuration)
- [Performance Metrics](#performance-metrics)
- [Model Checkpoints](#model-checkpoints)
- [Video Generation](#video-generation)
- [Conclusion](#conclusion)
- [Future Considerations](#future-considerations)

## Dataset Acquisition

The Anime Face Dataset is downloaded using the `opendatasets` library from Kaggle. The dataset is stored in the project directory, and basic checks are performed to ensure successful acquisition.

## Data Preprocessing

Images in the dataset are preprocessed using PyTorch's `ImageFolder` and `DataLoader`. Transformations such as resizing, center cropping, normalization, and tensor conversion are applied.

## Data Visualization

The `show_batch` function is used to visualize a batch of images from the training set, providing insights into the anime face samples.

## Device Handling

Functions for selecting the default device and moving data to the chosen device are implemented to ensure compatibility with both GPU and CPU.

## Model Architecture

The project includes the creation of the generator and discriminator using PyTorch's neural network module. The discriminator distinguishes between real and generated images, while the generator aims to produce realistic anime face images.

## Training the GAN

The training process is divided into functions for training the discriminator and generator. The GAN is trained iteratively to find a balance where the generator produces convincing images, and the discriminator accurately classifies between real and fake samples.

## Results and Visualization

Generated images are showcased at different stages of training. Random latent tensors are initially used, and as training progresses, the generator becomes capable of producing more realistic anime face images.

## Hyperparameters and Training Configuration

Hyperparameters such as learning rate and the number of epochs are logged using the `jovian` library, providing a clear record of the training configuration.

## Performance Metrics

Key metrics, including generator and discriminator losses, as well as real and fake scores, are logged and visualized throughout the training process to assess the performance and convergence of the GAN.

## Model Checkpoints

Trained model checkpoints for both the generator (`G.pth`) and discriminator (`D.pth`) are saved. These checkpoints can be loaded for further training or generating new samples.

## Video Generation

Generated images are compiled into a video file (`gans_training.avi`) to provide a dynamic view of the image generation process.

## Conclusion

The project successfully demonstrates the generation of anime face images using GANs. The README provides a comprehensive overview of the entire process, and the generated images showcase the evolving capabilities of the GAN over the training epochs.

## Future Considerations

To enhance the project, future considerations may include experimenting with different GAN architectures, tuning hyperparameters, or exploring advanced techniques for stabilizing GAN training.

