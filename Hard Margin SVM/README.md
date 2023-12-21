# SVM Implementation Report

## What I did:

I attempted to implement SVM from scratch.

## Linearly Separable Dataset Creation:

Utilized 'Danceability' and 'Energy' features for dataset creation and established a 'Danceability' threshold for binary class assignment.

## Non-Linearly Separable Dataset Creation:

Generated a non-linearly separable dataset with randomized class assignment.

## Hard Margin SVM Implementation:

Implemented a hard margin SVM for both datasets.

## Application on Linear Separable Dataset:

Trained a hard margin linear SVM on the linearly separable dataset and printed the accuracy of the trained model.

## Application on Non-Linear Separable Dataset:

Trained a hard margin linear SVM on the non-linearly separable dataset and printed the accuracy of the trained model.

## Accuracy Discussion:

### Linearly Separable Dataset:

The linear SVM performed well on the linearly separable dataset. The nature of the dataset allowed the SVM to easily find an optimal hyperplane, resulting in a high accuracy score.

### Non-Linearly Separable Dataset:

The linear SVM faced challenges on the non-linearly separable dataset. The introduced randomness made it difficult for the model to find a single straight line to separate the classes perfectly. This highlights the limitations of linear models in capturing complex, non-linear relationships.

## Errors and Issues:

### Linearly Separable Dataset:

While training the SVM on the linearly separable dataset, I encountered convergence warnings. To address this, I increased the maximum number of iterations (`max_iter`) to ensure convergence. Additionally, I standardized and imputed missing values in the dataset.

### Non-Linearly Separable Dataset:

Similar to the linearly separable dataset, convergence warnings were observed during training on the non-linearly separable dataset. To mitigate this, I increased the maximum number of iterations. However, it's crucial to note that a linear SVM has inherent limitations in handling non-linear data.

## Limitations of Hard Margin SVM:

The hard margin SVM assumes that the data is linearly separable, which may not hold true in many real-world scenarios. Furthermore, the model's sensitivity to outliers can impact performance, especially in the presence of non-linear relationships. In such cases, kernel methods or a transition to soft margin SVMs may be more suitable.
