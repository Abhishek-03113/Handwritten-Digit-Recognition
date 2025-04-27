
# Handwritten Digit Recognition

This project implements a deep learning model to recognize handwritten digits using the MNIST dataset. The model is built using TensorFlow and Keras and achieves high accuracy in classifying digits from 0 to 9.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Preprocessing](#preprocessing)
- [Training](#training)
- [Evaluation](#evaluation)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Results](#results)
- [Acknowledgments](#acknowledgments)

## Overview
The goal of this project is to classify handwritten digits using a neural network. The MNIST dataset is used for training and testing the model. The project includes data preprocessing, model training, evaluation, and visualization of predictions.

## Dataset
The MNIST dataset is used, which contains:
- 60,000 training images
- 10,000 testing images

Each image is a grayscale 28x28 pixel representation of a handwritten digit.

## Model Architecture
The model is a feedforward neural network with the following layers:
1. **Flatten Layer**: Converts the 28x28 input images into a 1D array of 784 features.
2. **Dense Layer 1**: Fully connected layer with 512 neurons and ReLU activation.
3. **Dense Layer 2**: Fully connected layer with 512 neurons and ReLU activation.
4. **Output Layer**: Fully connected layer with 10 neurons (one for each digit) and softmax activation.

## Preprocessing
1. **Scaling**: The pixel values are scaled from 0-255 to 0-1.
   ```python
   x_train = x_train / 255
   x_test = x_test / 255
   ```
2. **Categorical Encoding**: The labels are one-hot encoded.

## Training
The model is compiled with:
- **Loss Function**: Categorical Crossentropy
- **Optimizer**: Adam
- **Metrics**: Accuracy

The model is trained for 10 epochs with a validation split of 20%.

## Evaluation
The model is evaluated on the test set using:
- **Accuracy**: To measure the overall performance.
- **Confusion Matrix**: To gain detailed insights into the model's performance for each digit.

## Dependencies
- Python 3.11.4
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- OpenCV

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/Abhishek-03113/Handwritten-Digit-Recognition
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   Open and execute `MSINT.ipynb` to train and evaluate the model.

## Results
- **Accuracy**: The model achieves an accuracy of **97.77%** on the test set.
- **Confusion Matrix**: Provides detailed insights into the model’s strengths and areas for improvement across different digits.

## Acknowledgments
- The MNIST dataset is provided by Yann LeCun and collaborators.
- TensorFlow and Keras are used for building and training the model.
