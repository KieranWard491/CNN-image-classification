# CNN Image Classification with PyTorch

A deep learning project exploring image classification using Convolutional Neural Networks (CNNs) on the CIFAR-10 dataset. This project was completed as part of Griffith University's Deep Learning course and investigates how network depth, learning rate, and mini-batch size influence model performance.

## Overview

The goal of this project was to design, train, and evaluate neural network architectures for image classification. A Softmax Regression model was implemented as a baseline and compared against a custom CNN architecture.

The project explores:

- Softmax Regression as a linear baseline
- Convolutional Neural Networks (CNNs)
- Residual Connections
- Batch Normalisation
- Dropout Regularisation
- Learning Rate Tuning
- Mini-batch Size Analysis
- Network Depth Analysis

## Dataset

The project uses the CIFAR-10 dataset, which contains:

- 60,000 colour images
- 10 object classes
- Image size: 32 × 32 pixels
- Training set: 45,000 images
- Validation set: 5,000 images
- Test set: 10,000 images

Classes include:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

## Technologies Used

- Python
- PyTorch
- NumPy
- Matplotlib
- Torchvision
- Jupyter Notebook

## Model Architectures

### Softmax Regression

A simple linear classifier used as a baseline model.

- Fully connected layer
- Cross-Entropy Loss
- SGD Optimiser

### Convolutional Neural Network

Custom CNN architecture featuring:

- Variable network depth
- Batch Normalisation
- ReLU Activations
- Residual Connections
- Dropout Regularisation
- Weight Decay

## Experiments

### 1. Network Depth Analysis

Models were evaluated with:

- 2 Convolutional Layers
- 8 Convolutional Layers
- 16 Convolutional Layers
- 32 Convolutional Layers

Regularised and non-regularised versions were compared to investigate overfitting and gradient flow in deeper networks.

### 2. Learning Rate Analysis

Learning rates tested:

- 0.000001
- 0.0001
- 0.001
- 0.01
- 1.0

The experiment demonstrated the impact of learning rate on convergence speed and training stability.

### 3. Mini-batch Size Analysis

Batch sizes tested:

- 1
- 8
- 16
- 64
- 256

This experiment explored the trade-off between computational efficiency, training stability, and model performance.

## Results

| Model | Validation Accuracy |
|---------|---------|
| Softmax Regression | ~40% |
| CNN (16 Layers) | ~80% |
| Final Regularised CNN | ~77% |
| Final Test Accuracy | 76.79% |

## Training Curves

### Final Regularised CNN

[Final Model Results](results/Final_Best_Model.png)

### Softmax Regression Baseline

[Softmax Regression Results](results/Softmax_Regression.png)

## Key Findings

### Network Depth

- Increasing depth improved performance up to 16 layers.
- Very shallow networks exhibited significant overfitting.
- Deep networks benefited from residual connections and regularisation techniques.

### Learning Rate

- 0.001 provided the best balance between convergence speed and stability.
- Extremely small learning rates resulted in slow learning.
- Large learning rates caused unstable training and divergence.

### Mini-batch Size

- Larger batch sizes produced smoother training curves.
- Batch size 256 achieved the best overall performance.
- Batch size 1 introduced significant gradient noise and computational overhead.

## Repository Structure


cnn-image-classification/
│
├── README.md
├── deep_learning_CNN.ipynb
├── deep_learning_CNN_report.docx
│
├── results/
│   ├── Softmax_Regression.png
│   └── Final_Best_Model.png
│
└── requirements.txt


## Learning Outcomes

This project provided practical experience with:

- Deep Learning fundamentals
- CNN architecture design
- Hyperparameter tuning
- Model evaluation and validation
- Regularisation techniques
- PyTorch development workflows
- Experimental analysis and reporting

## Author

**Kieran Ward**

Computer Science Student | Cybersecurity & AI Enthusiast
