# Customer Segmentation and Predictive Analysis

## Overview
This project focuses on analyzing customer data using unsupervised and supervised learning techniques. The goal is to identify meaningful customer segments and build a predictive model to enhance customer acquisition strategies. The project involves preprocessing, dimensionality reduction, clustering, and classification.

---

## Key Features

### Unsupervised Learning
1. **Data Preprocessing**:
   - Combined customer and azdias datasets after handling missing values, encoding high-dimensional features, and one-hot encoding.
   - Resulting dataset: 962,756 rows × 2,390 columns.
2. **Dimensionality Reduction**:
   - Used Truncated SVD to reduce dimensions of the azdias dataset due to memory constraints.
3. **Clustering**:
   - Determined optimal clusters (K=15) using visualization.
   - Analyzed cluster centroids to highlight differences between azdias and customers.
4. **Feature Analysis**:
   - Identified features contributing to significant principal components (e.g., PC6).
   - Conducted statistical analysis to uncover differences between azdias and customers.

### Supervised Learning
1. **Feature Selection**:
   - Applied variance thresholding post one-hot encoding, reducing features from 2,222 to 1,846.
2. **Class Imbalance Handling**:
   - Addressed class imbalance using `compute_class_weight`.  Overall was not sucessfull.  next step would be to try a SMOTE method.
3. **Modeling**:
   - Used CatBoostClassifier with hyperparameter tuning via Optuna.
   - Performed k-fold cross-validation for model evaluation.
4. **Model Performance**:
   - High precision for the dominant class, but poor performance on rare positive classes.
   - Next steps include exploring SMOTE for imbalance correction and testing alternative models.

---

## Setup Instructions

### Prerequisites
Ensure you have Python (>=3.8) installed along with the required libraries. Use the following steps to set up your environment:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/johmicrot/udacity_aws_nanodegree_capstone
   cd udacity_aws_nanodegree_capstone
   ```

2. **Run Jupyter lab**:
   Launch the notebooks for exploration:
   ```bash
   jupyter lab
   ```

4. **Execute the Scripts**:
   - **Unsupervised Learning**:
     Open and run `EDA_with_UnsupervisedLearning.ipynb`.
   - **Supervised Learning**:
     Open and run `SupervisedLearning.ipynb`.

---

Feel free to reach out with questions or suggestions.

