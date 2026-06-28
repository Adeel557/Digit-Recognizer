# Handwritten Digit Recognizer (CNN)

## Overview
This project is an image classification model that uses a deep Convolutional Neural Network (CNN) to accurately recognize and classify handwritten digits[cite: 3]. The pipeline includes a custom-built Grid Search function to systematically identify the optimal hyperparameters for model training, ensuring high accuracy and efficiency[cite: 3].

## Tech Stack
* **Language:** Python
* **Deep Learning Framework:** TensorFlow / Keras[cite: 3]
* **Data Processing & Visualization:** NumPy, Matplotlib[cite: 3]
* **Environment:** Jupyter Notebook

## Model Architecture
The sequential CNN architecture is designed to extract spatial hierarchies of features from 28x28 grayscale images[cite: 3]:
* **Input Layer:** 28x28x1 image matrices[cite: 3].
* **Convolutional Layers:** Three `Conv2D` layers (32 and 64 filters, 3x3 kernel) using `tanh` activation to extract localized feature maps[cite: 3].
* **Pooling Layers:** Two `MaxPooling2D` (2x2) layers for spatial down-sampling and dimensionality reduction[cite: 3].
* **Fully Connected Layers:** A `Flatten` layer followed by a `Dense` hidden layer (64 neurons, `tanh` activation)[cite: 3].
* **Output Layer:** A `Dense` layer with `softmax` activation to output probability distributions across the 10 target classes[cite: 3].

## Training & Hyperparameter Tuning
To maximize performance, the model's configuration was optimized using a programmatic Grid Search algorithm iterating through `itertools.product`[cite: 3]. The search tested multiple combinations of optimizers, activation functions, and filter sizes[cite: 3]. 
* **Optimal Optimizer:** Adam[cite: 3]
* **Optimal Activation:** Tanh[cite: 3]
* **Epochs:** 10[cite: 3]
* **Batch Size:** 32[cite: 3]

## Performance & Results
The final optimized model was trained and evaluated on unseen test data, achieving highly accurate classification metrics[cite: 3]. The trained weights are saved in a production-ready `convolutional_model.h5` format[cite: 3].
* **Test Accuracy:** 98.33%[cite: 3]
* **Test Loss:** 0.0649[cite: 3]
