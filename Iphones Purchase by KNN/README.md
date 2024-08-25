### Project Overview
This project involves using the K-Nearest Neighbors (KNN) algorithm to predict whether a customer will purchase an iPhone based on their gender, age, and salary. The dataset contains 400 records with four columns: Gender, Age, Salary, and Purchase iPhone. The objective is to build a predictive model that can accurately classify whether a customer will purchase an iPhone.

### Dataset
The dataset used in this project consists of the following columns:
1. **Gender**: The gender of the customer (Male or Female).
2. **Age**: The age of the customer.
3. **Salary**: The annual salary of the customer.
4. **Purchase iPhone**: A binary indicator where 1 means the customer purchased an iPhone, and 0 means they did not.

### Data Preprocessing
1. **Label Encoding**: The 'Gender' column, which is categorical, was converted to numerical values using Label Encoding.
   - Male = 1
   - Female = 0

2. **Splitting the Dataset**: The dataset was split into training and testing sets using an 80-20 ratio.

3. **Feature Scaling**: Standardization was applied to the 'Age' and 'Salary' features to ensure they are on the same scale, which is crucial for the performance of KNN.

### Model Training and Evaluation
1. **Initial KNN Model**:
   - The initial KNN model was trained using `n_neighbors=1`.
   - The model's performance was evaluated on the test set, resulting in an accuracy of **88%**.

   **Classification Report**:
   - **Precision**:
     - Class 0: 0.92
     - Class 1: 0.76
   - **Recall**:
     - Class 0: 0.92
     - Class 1: 0.76
   - **F1-Score**:
     - Class 0: 0.92
     - Class 1: 0.76

2. **Hyperparameter Tuning**:
   - To determine the best value of `k`, an error rate was calculated for `k` values ranging from 1 to 39.
   - The error rate plot indicated that `k=7` provided the lowest error rate.

3. **Final KNN Model**:
   - The model was retrained with `n_neighbors=10`, which was selected based on cross-validation.
   - The accuracy of the final model improved to **93%**.

   **Classification Report**:
   - **Precision**:
     - Class 0: 0.93
     - Class 1: 0.90
   - **Recall**:
     - Class 0: 0.96
     - Class 1: 0.83
   - **F1-Score**:
     - Class 0: 0.95
     - Class 1: 0.86

### Cross-Validation
- A 10-fold cross-validation was conducted to validate the model's performance for different values of `k`.
- The best `k` was found to be **1** based on the average accuracy across the folds.

### Accuracy Plot
- A plot of accuracy versus the number of neighbors (k) was generated to visualize the model's performance with varying `k` values.

### Conclusion
The K-Nearest Neighbors algorithm was effective in predicting iPhone purchases with an accuracy of **93%**. Hyperparameter tuning played a critical role in improving the model's performance. This project demonstrates the importance of selecting the appropriate `k` value in KNN and the benefits of using cross-validation for model evaluation.

