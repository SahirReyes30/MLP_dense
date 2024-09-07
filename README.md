# MLP_dense
This repository contains an implementation of a Multilayer Perceptron (MLP) using Keras and TensorFlow, designed for **binary classification** problems. It also includes instructions for using `plaidml` to enable GPU acceleration on Radeon graphics cards.

## Model Architecture
- **Input Layer:** `Dense(64, input_dim=20, activation='relu')`
- **Hidden Layers:** `Dense(64, activation='relu')`
- **Output Layer:** `Dense(1, activation='sigmoid')`

## GPU Acceleration with PlaidML (for Radeon GPUs)  
To run this model using your Radeon GPU, you can configure Keras to use `plaidml`. Follow these steps:  
1. Install PlaidML:  
   `pip install plaidml-keras plaidml`  
2. Set PlaidML as the backend:  
   `plaidml-setup`  
3. In your Python script, import `plaidml.keras` instead of the regular Keras:  
   `import plaidml.keras`  
   `plaidml.keras.install_backend()`  
   `from keras.models import Sequential`  
   `from keras.layers import Dense`  

## Usage  
1. Clone the repository.  
2. Adjust the input data for your specific problem.  
3. Train the model with your dataset.  

This setup allows you to leverage your Radeon GPU for faster training and inference on binary classification tasks.
