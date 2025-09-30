Fashion MNIST Classifier using Customized Residual CNN in TensorFlow

This project implements a high-accuracy clothing image classifier using the Fashion MNIST dataset. Built with TensorFlow and Keras, the model leverages a customized residual CNN architecture with batch normalization, achieving ~99% test accuracy. It demonstrates efficient feature extraction and robust classification.

Dataset Overview

The [Fashion MNIST dataset](https://github.com/zalandoresearch/fashion-mnist) consists of 70,000 grayscale images (28×28 pixels), categorized into 10 fashion classes.

Training samples**: 60,000  
Test samples**: 10,000  
Image size**: 28x28 (grayscale)  
Classes:
  - 0: T-shirt/top
  - 1: Trouser
  - 2: Pullover
  - 3: Dress
  - 4: Coat
  - 5: Sandal
  - 6: Shirt
  - 7: Sneaker
  - 8: Bag
  - 9: Ankle boot

Model Architecture

Built using TensorFlow/Keras Functional API:

- Input: `(28, 28, 1)`
- `Conv2D` → `BatchNormalization`
- `Conv2D` → `BatchNormalization`
- `Add` (Residual Connection)
- `MaxPooling2D`
- `Flatten`
- `Dense(128)` → `BatchNormalization`
- `Dense(10)` (Softmax)

Model Summary:
- Total Parameters: `2,442,944`
- Trainable: `814,186`
- Test Accuracy: ~99%

---

Training Performance

- Final Accuracy: 99%
- Final Loss: Low and stable
- Model generalizes well to unseen data
