# Dimensionality-Reduction-PCA

### Step 1: Standardization
- Ensure all variables contribute equally to the analysis by standardizing their ranges.
- Subtract the mean and divide by the standard deviation for each variable.
- Prevents bias in PCA due to differences in variable ranges.

### Step 2: Covariance Matrix Computation
- Objective: Understand relationships between variables; identify correlations.
- Process: Compute the covariance matrix, a symmetric matrix showing covariances between all variable pairs.
- Interpretation: Positive covariance indicates variables increase/decrease together; negative indicates an inverse correlation.

### Step 3: Compute Eigenvalues and Eigenvectors of Covariance Matrix
- Objective: Identify principal components (new uncorrelated variables) that capture most information.
- Concepts: Eigenvectors are directions of maximal variance (principal components); eigenvalues are coefficients indicating the amount of variance.
- Implementation: Rank eigenvectors by corresponding eigenvalues; higher eigenvalues indicate more significant principal components.
##### `hint` : `The eigenvectors of the covariance matrix represent the directions of maximum variance in the dataset. These eigenvectors are considered characteristic or "own" to the covariance matrix because they define the principal components that capture the most significant information about the data.`

### Step 4: Feature Vector
- Objective: Choose significant principal components for dimensionality reduction.
- Process: Form a feature vector with selected eigenvectors; discard less significant components if desired.
- Importance: Feature vector is the first step towards dimensionality reduction; retains most important information.

### Step 5: Recast the Data Along the Principal Components Axes
- Reorient data from original axes to principal components axes.
- Implementation: Multiply the transpose of the original data set by the transpose of the feature vector.
- Result: Represents data in terms of new, uncorrelated variables (principal components).