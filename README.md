# Resume Screening & ATS Hiring Prediction

## Project Overview

This project analyzes a 100,000-record Resume Screening and ATS Hiring dataset to identify factors associated with candidate selection and develop machine learning and deep learning models for predicting whether a candidate is selected or rejected.

The project combines exploratory data analysis, statistical hypothesis testing, machine learning, model tuning, error analysis, and an Artificial Neural Network (ANN) to evaluate different approaches to candidate selection prediction.

The main objective is not only to build a predictive model, but also to understand which candidate characteristics and assessment measures are most strongly associated with the selection outcome.

---

## Dataset

**Dataset:** Resume Screening & ATS Hiring Dataset (100k Records)

**Source:** Kaggle  
**Dataset creator:** mobeenfatimah

The dataset contains:

- 100,000 candidate records
- 44 original variables
- Candidate demographic information
- Education information
- Professional experience
- Technical skills
- Assessment scores
- Resume quality measures
- ATS-related measures
- Job information
- Candidate selection outcome

### Target Variable

The target variable is:

`selected`

with two classes:

- `Selected`
- `Rejected`

The target was perfectly balanced:

| Class | Records | Percentage |
|---|---:|---:|
| Rejected | 50,000 | 50% |
| Selected | 50,000 | 50% |

Therefore, no class-balancing technique was required.

---

# Project Objectives

The project aims to:

1. Explore the structure and quality of the dataset.
2. Identify relationships between candidate characteristics and selection.
3. Investigate numerical and categorical variables using statistical hypothesis testing.
4. Prepare appropriate features for machine learning.
5. Train and compare multiple classification models.
6. Tune the strongest traditional machine learning model.
7. Perform model error analysis.
8. Develop a deep learning ANN model.
9. Compare traditional machine learning and deep learning approaches.
10. Identify important factors associated with candidate selection.

---

# Project Workflow

```text
Data Loading
     ↓
Data Understanding & Cleaning
     ↓
Exploratory Data Analysis
     ↓
Relationship Analysis
     ↓
Hypothesis Testing
     ↓
Feature Selection & Preparation
     ↓
Train/Test Split
     ↓
Traditional Machine Learning
     ↓
Model Comparison
     ↓
Gradient Boosting Tuning
     ↓
Error Analysis
     ↓
Deep Learning ANN
     ↓
Final Model Comparison
     ↓
Interpretation & Conclusions
