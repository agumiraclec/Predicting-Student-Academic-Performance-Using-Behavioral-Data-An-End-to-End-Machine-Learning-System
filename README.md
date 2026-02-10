# 🎓 Student Academic Performance Predictor

**Live Demo:** [Hugging Face Space](https://huggingface.co/spaces/Lion-agu/student-performance-predictor)

---

## Project Overview

This project is an **end-to-end machine learning system** designed to predict student exam scores using behavioral, lifestyle, and academic indicators. The system demonstrates the full data science lifecycle, including data cleaning, exploratory data analysis (EDA), feature engineering, model training and comparison, hyperparameter tuning, model serialization, and deployment through a user-friendly Streamlit web application.

---

## Dataset

The dataset contains approximately **1,000 student records** with the following attributes:

**Numerical Features:**
- `age`
- `study_hours_per_day`
- `social_media_hours`
- `netflix_hours`
- `attendance_percentage`
- `sleep_hours`
- `exercise_frequency`
- `mental_health_rating`

**Categorical Features:**
- `gender`
- `part_time_job`
- `diet_quality`
- `parental_education_level`
- `internet_quality`
- `extracurricular_participation`

**Target Variable:**
- `exam_score` (0–100)

The data captures both **demographics and lifestyle behaviors** that influence academic performance.

---

## Data Analysis & EDA

Key steps performed on the dataset:

- Checked for missing values, duplicates, and data types
- Performed **univariate analysis** (histograms, counts)
- Performed **bivariate analysis** (scatter plots, boxplots)
- Generated **correlation heatmaps** to understand relationships between features and target
- Selected features based on relevance and predictive strength

Visualizations were created using **Matplotlib** and **Seaborn** to support feature selection and interpretation.

---

## Feature Engineering

- Encoded categorical variables (e.g., `part_time_job`) using `LabelEncoder`
- Selected the most predictive features for modeling:
  - `study_hours_per_day`
  - `attendance_percentage`
  - `mental_health_rating`
  - `sleep_hours`
  - `part_time_job`

This step ensured **model interpretability and performance**.

---

## Model Training & Evaluation

Multiple regression models were trained and compared using **scikit-learn**:

- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**

**Process:**
- Split data into training and testing sets (80/20)
- Used **GridSearchCV** for hyperparameter tuning
- Evaluated models using **RMSE** and **R²** metrics
- Selected the best-performing model based on RMSE

The final model was retrained on the **entire dataset** for deployment.

---

## Deployment

The trained model is deployed as a **Streamlit web application**, enabling real-time predictions:

- Users can input:
  - Study hours
  - Attendance percentage
  - Mental health rating
  - Sleep hours
  - Part-time job status
- The app predicts the student's exam score instantly
- Deployed live on Hugging Face Spaces: [Live App](https://huggingface.co/spaces/Lion-agu/student-performance-predictor)

---

## Tools & Technologies

- **Data Analysis & Visualization:** Python, Pandas, NumPy, Matplotlib, Seaborn  
- **Machine Learning:** Scikit-learn (Linear Regression, Decision Tree, Random Forest), GridSearchCV  
- **Model Serialization:** Joblib  
- **Deployment:** Streamlit, Hugging Face Spaces  

---

## Key Learnings

- Worked with a realistic, mixed-type dataset combining behavioral and academic factors
- Developed robust **data preprocessing and feature engineering pipelines**
- Applied **model selection and hyperparameter optimization**
- Deployed an interactive ML app accessible to non-technical users
- Practiced end-to-end ML workflow from **raw data → model → live application**
