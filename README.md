# GAN Image Generation

A deep learning project that implements a Generative Adversarial Network (GAN) to create realistic fashion images using TensorFlow and Keras.

## What This Project Does

This project trains two neural networks that compete against each other:
- **Generator**: Creates fake fashion images from random noise
- **Discriminator**: Tries to distinguish between real and fake images

Through this adversarial training process, the generator learns to create increasingly realistic fashion items like clothing, shoes, and accessories.

## Requirements

- Python 3.7+
- TensorFlow 2.x
- NumPy
- Matplotlib
- GPU recommended (training will be much faster)

Install dependencies:
```bash
pip install tensorflow numpy matplotlib
```

## How to Run

1. Open the Jupyter notebook in your preferred environment
2. Run all cells sequentially from top to bottom
3. The model will train for 50 epochs (takes 10-15 minutes on GPU, 2-3 hours on CPU)
4. Generated images and model checkpoints are saved automatically

## What You Get

After training, the project creates:
- generated_images/ folder with sample images from each training epoch
- generator_model.keras and discriminator_model.keras - saved trained models
- training_checkpoints/ folder with model checkpoints
- Loss curves showing training progress
- Final grid of 25 generated fashion images

## Key Features

- Uses Fashion MNIST dataset (70,000 grayscale fashion images)
- Implements DCGAN architecture with convolutional layers
- Includes batch normalization and dropout for stable training
- Tracks and visualizes training progress
- Saves models for future use

## Training Process

The notebook includes 13 main sections covering data preprocessing, model architecture, training loop, and result visualization. Training progress is displayed in real-time with loss values and sample generated images.

## Expected Results

Early epochs produce noisy, unclear images. By epoch 50, the generator creates recognizable fashion items that resemble the training data. The discriminator and generator losses should stabilize around 0.9-1.4 range.
