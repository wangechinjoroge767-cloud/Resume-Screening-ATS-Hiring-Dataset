# Resume-Screening-ATS-Hiring-Dataset
Machine learning project for analyzing resume screening and predicting candidate selection outcomes.


# Resume Screening & ATS Hiring Prediction

## Project Overview

This project analyzes a 100,000-record Resume Screening and ATS Hiring Dataset to identify patterns associated with candidate selection and develop machine learning models for predicting whether a candidate is selected or rejected.

The project combines:

- Exploratory Data Analysis (EDA)
- Descriptive statistics
- Statistical hypothesis testing
- Feature engineering
- Machine learning
- Hyperparameter tuning
- Model evaluation
- Feature importance analysis
- Error analysis

---

## Dataset

The dataset contains **100,000 candidate records and 44 original features** covering candidate demographics, education, professional experience, skills, assessments, resume characteristics, ATS metrics, and recruitment outcomes.

The target variable is:

- `selected` — whether the candidate was **Selected** or **Rejected**

The target was perfectly balanced:

| Outcome | Count | Percentage |
|---|---:|---:|
| Selected | 50,000 | 50% |
| Rejected | 50,000 | 50% |

### Dataset Source

The dataset was obtained from Kaggle:

**Resume Screening and ATS Hiring Dataset (100k Record)**

Dataset by `mobeenfatimah`.

The original dataset is not included in this repository.

---

## Project Objectives

The main objectives of this project were to:

1. Understand the characteristics of the candidate dataset.
2. Identify variables associated with candidate selection.
3. Investigate relationships between candidate characteristics and selection outcomes.
4. Statistically test observed differences and associations.
5. Develop machine learning models for predicting candidate selection.
6. Compare the performance of different classification algorithms.
7. Tune the strongest model using cross-validation.
8. Identify the features most influential to the final model.
9. Analyze model prediction errors.

---

## Exploratory Data Analysis

The EDA examined:

- Candidate demographics
- Education
- Professional experience
- Internship experience
- Leadership experience
- Previous company experience
- Technical skills
- Assessment scores
- ATS metrics
- Resume quality
- Keyword matching
- Expected salary
- Job roles
- Employment characteristics

### Key EDA Findings

Professional experience showed one of the strongest relationships with candidate selection.

Selected candidates generally had higher:

- Technical test scores
- Interview scores
- Problem-solving scores
- ATS scores
- Keyword-match percentages
- Resume quality scores

Internship experience, leadership experience, and previous company experience also showed positive associations with selection.

Several variables showed relatively weak relationships with selection, including employment type, remote preference, availability, gender, certifications, publications, and number of projects completed.

---

## Hypothesis Testing

Statistical testing was performed to determine whether observed differences and associations were supported by the data.

### Numerical Variables

The **Mann–Whitney U test** was used to compare numerical variables between selected and rejected candidates.

Variables tested included:

- Experience years
- Age
- Expected salary
- CGPA
- Technical test score
- Interview score
- Problem-solving score
- ATS score
- Keyword-match percentage
- Resume quality score

The largest effect sizes were observed for:

- Experience years
- Age
- Expected salary
- Technical test score
- Interview score

### Categorical Variables

The **Chi-square test of independence** was used to examine relationships between categorical variables and candidate selection.

The strongest categorical associations included:

- Experience group
- Current job title
- Leadership experience
- Previous company experience
- Internship experience

Cramér's V was used to examine the strength of categorical associations.

Statistical significance was interpreted alongside effect size because the large sample size means that very small differences can produce statistically significant results.

---

## Machine Learning

Five classification results were evaluated:

1. Logistic Regression
2. Decision Tree
3. Random Forest
4. Gradient Boosting
5. Tuned Gradient Boosting

### Model Comparison

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Logistic Regression | 80.65% | 80.31% | 81.19% | 80.75% |
| Decision Tree | 78.24% | 77.97% | 78.73% | 78.35% |
| Random Forest | 83.05% | 78.90% | 90.23% | 84.19% |
| Gradient Boosting | **84.19%** | **81.55%** | 88.38% | **84.83%** |
| Tuned Gradient Boosting | 84.16% | 81.44% | **88.48%** | 84.81% |

Gradient Boosting produced the strongest overall baseline performance.

---

## Hyperparameter Tuning

Gradient Boosting was tuned using `GridSearchCV` with 3-fold cross-validation.

The selected parameters were:

```text
n_estimators = 200
learning_rate = 0.05
max_depth = 3
