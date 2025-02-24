### Predictive Modeling of Protein Structure Using Deep Learning


## Overview
This project focuses on analyzing and predicting protein structure properties using machine learning techniques. It leverages protein data derived from 9-mers, including torsion angles (phi, psi) and 3D coordinates. The project preprocesses the dataset, builds a deep learning model, and visualizes model performance to gain insights into protein structure prediction.

## Dataset
The dataset used for this project consists of protein fragments of length nine, called 9-mers, derived from a publicly available dataset. It includes the following columns:
- protein_sequences: The numerical representation of protein sequences.
- phi_psi_angles: Torsion angles for each protein fragment.
- 3d_coordinates: 3D spatial coordinates representing protein structure.

## Data Source
The dataset is derived from the UCI Machine Learning Repository - 9mers from CullPDB.

## Preprocessing
The data preprocessing steps include:
- Mapping protein sequences to amino acid names using a provided amino acid order.
- Normalizing and reshaping torsion angles (phi, psi) using a tuple size of 2.
- Normalizing and reshaping 3D coordinates using a tuple size of 3.
- Filtering rows with valid processed data.
- Scaling the features using MinMaxScaler for improved model performance.


## Modeling
A deep learning model is built using TensorFlow and Keras with the following architecture:
- Input Layer: Accepts normalized torsion angles and 3D coordinates.
- Hidden Layers: Dense layers with ReLU activation and 128 and 64 neurons.
- Output Layer: Predicts values for the target based on input features.

The model is trained using:
1. Loss Function: Mean Squared Error (MSE)
2. Optimizer: Adam
3. Validation Split: 0.1
4. Epochs: 10

## Results
- The training and validation loss over epochs is plotted.
- The test loss for the model is calculated as approximately 0.0797, indicating the model's performance on unseen data.
- A histogram of predicted values shows the distribution of model outputs.


## Conclusion
1. The model shows promising results for predicting protein structure properties.
2. The current architecture is able to learn from the input features and generalize well to unseen data.
3. Further improvements can be made to enhance model performance and reduce overfitting.
