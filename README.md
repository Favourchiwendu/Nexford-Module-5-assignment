# Nexford-Module-5-assignment
# Breast Cancer Diagnosis using PCA and Logistic Regression

Thanks to Nexford and my instructor, I am glad i could apply the knowledge of PCA and Logistic regression into this project.

This project demonstrates the use of Principal Component Analysis (PCA) for dimensionality reduction and Logistic Regression for classification on the breast cancer Wisconsin dataset.

## 1. Data Loading and Preprocessing

The breast cancer dataset is loaded from scikit-learn.  The data is then converted to a Pandas DataFrame for easier manipulation.  Crucially, the features are standardized using `StandardScaler` before applying PCA.  Standardization ensures that features with larger values don't disproportionately influence the PCA results.


## 2. Dimensionality Reduction with PCA

PCA is applied to reduce the dimensionality of the dataset.  The optimal number of principal components is determined by analyzing the explained variance ratio. A plot of the cumulative explained variance ratio versus the number of components is generated to visualize the "elbow point," which suggests the number of components that capture most of the variance in the data. In this case, 2 principal components are selected.

The data is then projected onto the first two principal components and visualized using a scatter plot. This plot helps to see how well the two components separate the different classes (malignant and benign).

## 3. Logistic Regression Modeling

Logistic regression is trained on the data reduced to two principal components. The data is split into training and testing sets to evaluate the model's performance on unseen data.


## 4. Model Evaluation

The performance of the logistic regression model is assessed using accuracy and a classification report. The accuracy score provides an overall measure of correct predictions, while the classification report shows precision, recall, F1-score, and support for each class (malignant and benign).

## Results

The model achieves high accuracy, demonstrating the effectiveness of combining PCA for dimensionality reduction and logistic regression for classification. The use of PCA reduces the original 30 features to just 2, while maintaining excellent predictive performance, showcasing the power of dimensionality reduction techniques.
