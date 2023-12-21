# Regression Prediction with Neural Network

## Define the issue you are trying to address:

The code is attempting to address a regression problem. Specifically, it's trying to predict the number of 'Likes' for songs based on various audio and metadata features (e.g., 'Danceability', 'Energy', 'Key', 'Loudness', 'Speechiness', etc.). The goal is to build a neural network model that can make accurate predictions.

## Describe where and how you acquired the data and provide details on the type, size, and quality of the data:

- The data is acquired from a CSV file located at '/content/drive/MyDrive/Colab Notebooks/Spotify_Youtube.csv'. The data is in tabular format.
- The size of the data is not specified in the code, but it's assumed to contain a sufficient number of records for training and testing a machine learning model.
- The quality of the data is addressed by removing rows with missing values or non-numeric values in specific columns. This data preprocessing step ensures that the dataset is clean and suitable for machine learning.

## Neural Network implementation:

- The neural network architecture is implemented with one hidden layer, a specified number of units, and ReLU activation functions.
- Weights and biases are initialized with small random values.
- Hyperparameters like learning rate and the number of training epochs are defined.

## Learning algorithm implementation:

- The code implements a training loop that iterates for a specified number of epochs.
- During each epoch, it performs forward and backward propagation to update the weights and biases.
- Gradient clipping is applied to prevent gradient explosions.
- The code also calculates and prints the error (mean squared error) at regular intervals during training.

## Cross-validation Experiments:

The code does not explicitly implement cross-validation. It splits the data into a training set (80%) and a testing set (20%) to evaluate the model's performance.

## Normalization of the Target Variable:

Applied a logarithmic transformation to the 'Likes' target variable to mitigate issues related to large gradients and improve training stability.

## Loss Function:

Instead of using Mean Squared Error (MSE), I've adopted the Mean Absolute Error (MAE) as the loss function during both training and evaluation. MAE is known for its robustness in the presence of outliers and provides a more interpretable measure of prediction accuracy.

## Gradient Clipping:

Implemented gradient clipping to prevent exploding gradients during backpropagation. This addition is crucial for stabilizing the training process and ensuring the model converges effectively.

## Learning Rate Adjustment:

Adjusted the learning rate to 0.0001. This modification aims to control the step size during weight updates, contributing to a more stable and controlled training process.

## Cross-Validation:

Integrated k-fold cross-validation into the model evaluation process. This ensures a comprehensive assessment of the model's performance across different subsets of the dataset, enhancing its ability to generalize to unseen data.

The training progress and cross-validation results have shown promising outcomes, with an average MAE of approximately 1.92, average MSE of about 6.04, average RMSE around 2.46, and an average R^2 close to 0.02 across all folds.
