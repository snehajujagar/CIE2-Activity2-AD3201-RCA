# Student-Placement-Prediction-Logistic-Regression-RollNo---AD3201
A Machine Learning project that predicts student placement status using Logistic Regression. Includes data preprocessing, exploratory data analysis, feature scaling, model training, and evaluation with 80.60% accuracy.

# Student Placement Prediction Using Logistic Regression

## 1. Project Overview

This project focuses on predicting student placement status using Machine Learning techniques.

The project implements the Logistic Regression algorithm to classify engineering students into two categories: Placed and Not Placed.

The prediction is based on various student-related factors, including academic performance, technical skills, communication skills, internships, projects, certifications, and other activities.

The main objective is to analyze student data, perform data preprocessing, build a classification model, and evaluate its performance.

## 2. Objectives

- To understand and analyze the student placement dataset.
- To perform Exploratory Data Analysis (EDA).
- To identify and handle missing values.
- To perform data cleaning and preprocessing.
- To convert categorical data into numerical format.
- To apply feature scaling.
- To implement the Logistic Regression algorithm.
- To predict student placement status.
- To evaluate model performance using classification metrics.

## 3. Dataset Description

**Dataset Name:** Indian Engineering Placement Dataset 2026

**Dataset File:** `indian_engineering_placement_2026.csv`

The dataset contains 15,000 student records and 25 columns.

It includes information related to students' academic performance, technical skills, communication skills, internships, projects, extracurricular activities, and placement status.

### Important Features

| Feature | Description |
|---|---|
| Age | Age of the student |
| Gender | Gender of the student |
| State | State of the student |
| Branch | Engineering branch |
| College_Tier | College category |
| CGPA | Academic performance |
| Attendance_Percentage | Attendance percentage |
| DSA_Problems_Solved | Number of DSA problems solved |
| Aptitude_Score | Aptitude test score |
| Communication_Score | Communication skills score |
| Projects_Count | Number of projects |
| Internships_Count | Number of internships |
| Certifications_Count | Number of certifications |
| GitHub_Contributions | GitHub contributions |
| LinkedIn_Activity_Score | LinkedIn activity score |
| Hackathons_Participated | Number of hackathons |
| Soft_Skills_Score | Soft skills score |
| Placement_Status | Final placement status |

**Target Variable:** `Placement_Status`

The target variable contains two classes:

- 0 = Not Placed
- 1 = Placed

**Dataset Source:** The notebook uses the local CSV file `indian_engineering_placement_2026.csv`. An external dataset source URL is not specified in the notebook.

## 4. Technologies and Libraries Used

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

## 5. Project Workflow

### Step 1: Data Loading

- Imported the required Python libraries.
- Loaded the dataset using Pandas.
- Displayed the first five records.
- Checked dataset shape, columns, and information.
- Generated statistical summaries.

### Step 2: Exploratory Data Analysis (EDA)

Performed exploratory data analysis to understand the dataset.

- Checked dataset dimensions.
- Examined column names and data types.
- Generated statistical summaries.
- Checked missing values.
- Checked duplicate records.
- Analyzed placement status distribution.
- Created count plots and box plots.
- Studied the relationship between CGPA, attendance, and placement status.

### Step 3: Data Cleaning and Preprocessing

- Checked missing values in the dataset.
- Handled missing values in `Open_Source_Contributions` using median.
- Handled missing values in `LinkedIn_Activity_Score` using median.
- Removed unnecessary columns such as `Student_ID` and `Package_LPA`.
- Applied One-Hot Encoding to categorical features.
- Converted the target variable into binary format.

### Step 4: Feature Preparation and Scaling

- Separated independent variables (X) and dependent variable (y).
- Applied One-Hot Encoding using Pandas.
- Prepared 48 input features for model training.
- Applied StandardScaler for feature scaling.

### Step 5: Train-Test Split

The dataset was divided into training and testing sets.

- Training Data: 80% (12,000 records)
- Testing Data: 20% (3,000 records)
- Random State: 42
- Stratified sampling was used to maintain class distribution.

### Step 6: Model Building

**Algorithm: Logistic Regression**

Logistic Regression is a supervised Machine Learning classification algorithm used to predict categorical outcomes.

In this project, Logistic Regression is used to classify students into two categories:

- Placed
- Not Placed

The following steps were performed:

- Created a Logistic Regression model.
- Set maximum iterations to 1000.
- Trained the model using the training dataset.
- Generated predictions using the testing dataset.

### Step 7: Model Evaluation

The model was evaluated using the following performance metrics:

**1. Accuracy**

Measures the overall percentage of correct predictions.

**2. Confusion Matrix**

Shows the correct and incorrect predictions made by the model.

**3. Precision**

Measures how many predicted positive results are actually positive.

**4. Recall**

Measures how many actual positive cases are correctly identified.

**5. F1-Score**

Provides a balance between precision and recall.

## 6. Model Performance Results

The Logistic Regression model achieved the following results on the test dataset.

| Evaluation Metric | Result |
|---|---:|
| Accuracy | 80.60% |
| Weighted Precision | 0.80 |
| Weighted Recall | 0.81 |
| Weighted F1-Score | 0.80 |

### Confusion Matrix

The confusion matrix obtained from the model:

| | Predicted Not Placed | Predicted Placed |
|---|---:|---:|
| Actual Not Placed | 724 | 322 |
| Actual Placed | 260 | 1694 |

### Classification Report

| Class | Precision | Recall | F1-Score |
|---|---:|---:|---:|
| Not Placed (0) | 0.74 | 0.69 | 0.71 |
| Placed (1) | 0.84 | 0.87 | 0.85 |

## 7. Prediction on New Student Data

The trained Logistic Regression model was also tested with a new sample student record.

The sample student details included:

- Age: 22
- CGPA: 8.5
- Attendance: 85%
- DSA Problems Solved: 200
- Aptitude Score: 80
- Communication Score: 85
- Projects: 3
- Internships: 2
- Certifications: 4

### Prediction Result

The model predicted:

**Student is likely to be Placed.**

| Prediction | Probability |
|---|---:|
| Not Placed | 1.37% |
| Placed | 98.63% |

## 8. Model Saving

The trained model and StandardScaler were saved using Joblib.

- `placement_model.pkl`
- `placement_scaler.pkl`

These files can be used for future predictions.

## 9. How to Run the Project

**Step 1:** Clone or download this repository.

**Step 2:** Install the required libraries.

```bash
pip install numpy pandas matplotlib seaborn scikit-learn joblib
```

**Step 3:** Open Jupyter Notebook.

```bash
jupyter notebook
```

**Step 4:** Open the project notebook.

**Step 5:** Keep the dataset file `indian_engineering_placement_2026.csv` in the same folder as the notebook.

**Step 6:** Run all cells to execute the project.

## 10. Conclusion

This project demonstrates the implementation of Logistic Regression for predicting engineering student placement status.

The project includes data loading, exploratory data analysis, data cleaning, preprocessing, feature scaling, model training, and performance evaluation.

The Logistic Regression model achieved an accuracy of 80.60% on the testing dataset.

This project provides practical understanding of Machine Learning classification techniques and demonstrates how student-related attributes can be used to predict placement outcomes.

## 11. Future Scope

- Experiment with other classification algorithms.
- Improve model performance through hyperparameter tuning.
- Compare different classification models.
- Develop a user-friendly interface for placement prediction.

## 12. Author Information

**Name:** Sneha Arvind Jujagar

**Branch:** Artificial Intelligence and Data Science

**Semester:** 3rd Semester

**College:** Zeal College of Engineering and Research (ZCOER), Pune

## 13. Faculty GitHub Reference

This project is prepared as part of the Machine Learning academic activity.

**Submission GitHub ID:**

[Complexiota - Faculty GitHub Profile](https://github.com/complexiota)

## 14. Repository Information

- Repository Type: Individual Student Project
- Repository Visibility: Public
- Project Domain: Machine Learning
- Algorithm Used: Logistic Regression
- Problem Type: Binary Classification
- Target: Student Placement Prediction
