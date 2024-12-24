# EAS-503 - Breast Cancer Prediction Project
This project aims to predict whether a tumor is malignant or benign using a dataset containing features extracted from fine needle aspirate (FNA) of breast mass. The process includes data exploration, machine learning experimentation, and deployment of the best-performing model.

---

## Other Important Links:
- **Streamlit App:** [Breast Cancer Prediction App](https://breastcancerpredictionn.streamlit.app/)  
- **GitHub Repository (ML Models):** [Breast Cancer Prediction](https://github.com/saivignesh-03/ML1)  
- **GitHub Repository (Streamlit):** [Streamlit App](https://github.com/saivignesh-03/streamlitapp)  
- **DagsHub Repository (Experiments):** [DagsHub Experiments](https://dagshub.com/saivignesh-03/Machinelearning/experiments)  
- **DagsHub MLflow Tracking:** [MLflow Experiment Tracking](https://dagshub.com/saivignesh-03/Machinelearning.mlflow/#/experiments/0?searchFilter=&orderByKey=attributes.start_time&orderByAsc=false&startTime=ALL&lifecycleFilter=Active&modelVersionFilter=All+Runs&datasetsFilter=W10%3D)

---

## 1. Steps Involved

### 1.1. Data Selection and Acquisition
- **Dataset:** Used a breast cancer dataset containing features extracted from FNA (e.g., radius, texture, smoothness, compactness) and a target variable indicating malignancy.  
- **Source:** Retrieved the dataset from OpenML (Dataset ID: 31) and stored it locally.  
- **Database Integration:** Leveraged a previously created SQLite database (`breast_cancer.db`) to fetch structured data using SQL queries.

---

### 1.2. Data Preparation and Exploration

#### Data Extraction:
- Combined multiple tables from the database to create a cohesive dataset.

#### Data Inspection:
- Checked for missing values and handled them appropriately.
- Analyzed feature distributions to identify patterns and outliers.
- Explored relationships between features and the target variable using visualizations.

#### Feature Transformation:
- Encoded categorical variables where necessary.
- Standardized numerical features to ensure consistency.

---

### 1.3. Machine Learning Experimentation

#### Pipeline Development:
- Created reusable machine learning pipelines for streamlined experimentation.

#### Experiments Conducted:
1. **Logistic Regression:** Baseline model to establish initial performance.
2. **Random Forest:** Improved performance and identified as the best-performing model.

#### Feature Engineering:
- Introduced domain-specific features to improve prediction accuracy.

#### Feature Selection:
- Retained only the most impactful features based on feature importance scores.

#### PCA Dimensionality Reduction:
- Applied Principal Component Analysis to further reduce dimensionality and eliminate noise.

#### Feature Scaling:
- Normalized features to maintain uniformity for algorithms sensitive to magnitude.

#### Polynomial Features:
- Augmented feature space by generating interaction terms and polynomial terms.

#### Metrics Tracking:
- Logged experiments and evaluated models using MLflow integrated with DagsHub.

#### Model Selection:
- Random Forest was identified as the best model based on metrics like accuracy, precision, recall, and F1 score.

---

### 1.4. Model Deployment

#### Hosting:
- Packaged the Random Forest pipeline into a FastAPI application.
- Deployed the API on a cloud platform (DigitalOcean) to serve predictions.

#### User Interface:
- Built a Streamlit web application to provide an interactive interface for users.
- Integrated the app with the deployed FastAPI endpoint to facilitate real-time predictions.

---

### 1.5. Tools and Technologies Used
- **Data Handling:** Python (`pandas`, `SQLite3`), SQL  
- **Modeling and Logging:** scikit-learn, MLflow, DagsHub  
- **Deployment:** FastAPI, Streamlit, DigitalOcean  

---

### 1.6. Project Outcomes
- Successfully developed a robust machine learning pipeline for predicting malignancy in breast tumors.  
- Deployed a scalable API and a user-friendly web application for real-time predictions.  

---

### 1.7. Files and Artifacts
- **Notebook:** Contains EDA, feature engineering, and model experimentation steps.  
- **API:** FastAPI implementation for serving predictions.  
- **Web App:** Streamlit code for user interaction.  
- **Database:** SQLite database (`breast_cancer.db`) for fetching and preparing data.  
