# Analysis Report

## Libraries and Packages Used:

**numpy (np):**
Used for various numerical operations, such as handling NaN or Inf values, standardization, computing eigenvalues/eigenvectors, and more.

**pandas (pd):**
Used for reading the dataset from an Excel file and extracting relevant features.

**matplotlib.pyplot (plt):**
Used for creating visualizations, including box plots, scatter plots for PCA and MDS results, and displaying the correlation matrix.

## Restrictions:

### Data Preprocessing and Eigenvalue Computation:

The code uses NumPy for data preprocessing (handling NaN or Inf values, standardization) and computes eigenvalues/eigenvectors using NumPy's np.linalg.eig function, meeting the restriction.

### Basic Vector Operations for PCA and MDS:

#### PCA:

The code uses basic vector operations (matrix multiplication) for projecting data onto the first two principal components, meeting the restriction.

#### MDS:

The code implements Classical MDS using basic vector operations (matrix multiplication). **classical_mds()** function uses basic vector operations for double centering, eigen decomposition, and constructing the low-dimensional representation.

### PCA Result Insights:

In examining the PCA result, I noticed that the first principal component (PC1) heavily weighs features like "Danceability," "Energy," and "Likes" in a negative direction. This suggests that songs with lower danceability, energy, and fewer likes contribute more to the variance in the dataset along PC1.

### MDS Result Findings:

The MDS result provides a pairwise distance-based representation, emphasizing local relationships between songs. This may reveal clusters or patterns not immediately apparent in the PCA visualization, offering a different perspective on how songs relate to each other.

### Correlation Matrix Implications:

The correlation matrix points to a strong positive correlation between "Likes" and "Views." This aligns with the PCA result, where the arrangement of points suggests that **songs with more likes also tend to have more views.**

## Hypotheses and Further Investigation:

My hypotheses include the idea that clusters in the PCA result might correspond to similar structures in the MDS result, indicating a consistency in global and local relationships. Additionally, the influence of highly correlated features like "Likes" and "Views" on the principal components, especially PC1, warrants further exploration. To validate these hypotheses, additional statistical analyses and possibly more visualizations or clustering methods could be employed.
