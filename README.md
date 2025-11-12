

# Student Performance Prediction

**Built a Random Forest Classifier to predict student performance, performing end-to-end data preprocessing and hyperparameter optimization. This project supports actionable educational interventions by improving model accuracy.**

## Table of Contents

- Project Overview
- Data
- Workflow
- Installation & Setup
- Usage
- Model Evaluation
- Results
- Future Work

## Project Overview

This project predicts student performance using machine learning techniques. It applies a Random Forest Classifier to a dataset (`student_performance.csv`), optimizing preprocessing and model parameters to achieve high accuracy. The workflow is designed for educators, data scientists, or researchers interested in leveraging data for educational insights.

## Data

- **Input:** `student_performance.csv`
    - The dataset should consist of features describing students and a target column representing performance (e.g., pass/fail, grades, etc.).

## Workflow

1. **Data Preprocessing**
    - Missing values are handled via imputation:
        - Numerical: Median imputation + scaling with StandardScaler.
        - Categorical: Imputation with 'missing' + one-hot encoding.
    - Features and target variable are separated.

2. **Pipeline Construction**
    - Combines preprocessing and model training into a single pipeline for consistency and reproducibility.

3. **Model Training & Evaluation**
    - Trains a Random Forest Classifier.
    - Evaluates initial accuracy, confusion matrix, and classification metrics on test data.

4. **Hyperparameter Tuning**
    - Uses GridSearchCV to find the best combination of hyperparameters.
    - Evaluates the tuned model's performance and compares it to the baseline.

## Installation & Setup

1. **Clone the repository**
    ```bash
    git clone https://github.com/Marshmallo-White/Student-Performance-Prediction-
    ```
2. **Install dependencies**
    ```bash
    pip install pandas numpy scikit-learn
    ```
3. **Place the dataset**
    - Put `student_performance.csv` in the project directory.

## Usage

1. **Run the script**
    ```bash
    python main.py
    ```
    - The script will:
        - Load and preprocess the data,
        - Train and tune the classifier,
        - Print metrics and accuracy improvement.

## Model Evaluation

- **Initial Model Metrics:**
    - Accuracy, Classification Report, Confusion Matrix.
- **Tuned Model Metrics:**
    - Improved accuracy and validation scores.
    - Confusion Matrix and Classification Report post-optimization.

## Results

- **Best Hyperparameters:** Printed in output.
- **Accuracy Improvement:** Displayed after tuning.
- **Reports:** Classification report and confusion matrix for both initial and tuned models.

## Future Work

- Add feature importance analysis.
- Try other models (e.g., SVM, XGBoost).
- Deploy as an interactive dashboard.
- Integrate additional student demographics or behavioral data.

## License

MIT

