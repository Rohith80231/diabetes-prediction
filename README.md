# diabetes-prediction

```markdown
# Diabetes Prediction Model

## Overview
This project implements a machine learning model to predict the likelihood of diabetes based on diagnostic measurements. The model utilizes a Support Vector Machine (SVM) classifier, trained and evaluated on a publicly available diabetes dataset.

## Dataset
The `diabetes.csv` dataset is used for this project. It contains various health parameters of patients and an `Outcome` column, which indicates the presence (1) or absence (0) of diabetes.

## Technologies Used
-   **Python**: The primary programming language.
-   **NumPy**: For numerical operations, especially with arrays.
-   **Pandas**: For efficient data manipulation and analysis.
-   **Scikit-learn**: A comprehensive library for machine learning, used for data preprocessing (scaling, splitting), model training (SVM), and evaluation (accuracy score).

## Project Workflow
The Jupyter Notebook (`diabetes_prediction.ipynb` - *you may rename this if your notebook has a different name*) follows these steps:

1.  **Data Loading**: The `diabetes.csv` dataset is loaded into a Pandas DataFrame.
2.  **Exploratory Data Analysis (EDA)**:
    *   Initial data inspection (`df.head()`, `df.shape`).
    *   Summary statistics (`df.describe()`).
    *   Analysis of the distribution of the target variable (`Outcome`).
    *   Calculation of mean feature values grouped by `Outcome` to observe differences between diabetic and non-diabetic groups.
3.  **Data Preprocessing**:
    *   Features (`X`) and the target variable (`Y`) are separated from the dataset.
    *   **Feature Scaling**: The features are standardized using `StandardScaler` to bring them to a common scale, which is crucial for SVM performance.
    *   **Data Splitting**: The dataset is divided into training and testing sets using `train_test_split` to ensure the model is evaluated on unseen data. A `stratify` parameter is used to maintain the same proportion of outcomes in both sets.
4.  **Model Training**:
    *   A Support Vector Machine (SVM) classifier is initialized with a linear kernel.
    *   The model is trained on the preprocessed training data (`X_train`, `Y_train`).
5.  **Model Evaluation**:
    *   The trained model's performance is assessed by calculating the accuracy score on both the training data and the test data.
6.  **Prediction Example**:
    *   A demonstration of how to use the trained model to make predictions for new, individual input data points. The input data is preprocessed (scaled) before being fed to the classifier.

## Results
The trained SVM model achieved an accuracy of approximately:
-   **Training Data Accuracy**: ~78.3%
-   **Testing Data Accuracy**: ~77.9%

## How to Use
1.  **Clone the Repository**:
    ```bash
    git clone <repository_url>
    cd <repository_name>
    ```
2.  **Install Dependencies**:
    Ensure you have Python installed, then install the required libraries:
    ```bash
    pip install numpy pandas scikit-learn
    ```
3.  **Dataset**: Place the `diabetes.csv` file in the root directory of the project, or update the file path in the notebook's data loading section.
4.  **Run the Notebook**: Open the Jupyter Notebook (`diabetes_prediction.ipynb` or your notebook's name) and run all cells sequentially to reproduce the analysis and model training.

```
