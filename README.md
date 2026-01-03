# Student Marks Predictor  
**End-to-End Machine Learning Project with Deployment**

---

## Abstract
The **Student Marks Predictor** is a production-ready, end-to-end machine learning application that predicts student marks based on input features.  
The project demonstrates real-world ML engineering practices including data pipelines, modular components, logging, exception handling, and web-based inference using a Flask application.

---

## Objective
To build a scalable machine learning system that:
- Ingests and processes raw student data
- Trains and evaluates a regression model
- Persists trained artifacts
- Serves predictions through a web interface

---

## Key Features
- End-to-end ML pipeline (training + inference)
- Modular and maintainable project structure
- Logging and custom exception handling
- Artifact and experiment tracking
- Flask-based web interface for predictions
- Deployment-ready architecture

---

## Project Architecture

MLPROJECT/
│
├── .ebextensions/
│   └── python.config
│
├── artifact/                     # Stored models, preprocessors, datasets
├── logs/                         # Application and pipeline logs
├── mlproject.egg-info/
│
├── notebook/
│   ├── data/
│   ├── EDA_STUDENT.ipynb         # Exploratory Data Analysis
│   └── MODEL_TRAINING.ipynb      # Model experimentation
│
├── src/
│   ├── components/
│   │   ├── init.py
│   │   ├── data_ingestion.py     # Data loading and splitting
│   │   ├── data_transformation.py# Feature engineering & preprocessing
│   │   └── model_trainer.py      # Model training and evaluation
│   │
│   ├── pipeline/
│   │   ├── init.py
│   │   ├── train_pipeline.py     # Training pipeline orchestration
│   │   └── predict_pipeline.py   # Inference pipeline
│   │
│   ├── exception.py              # Custom exception handling
│   ├── logger.py                 # Centralized logging
│   └── utils.py                  # Common utility functions
│
├── static/
│   └── style.css                 # Frontend styling
│
├── templates/
│   ├── home.html                 # Prediction input page
│   └── index.html                # Landing page
│
├── venv/                         # Virtual environment
├── .gitignore
├── app.py                        # Flask app entry point
├── application.py                # Application runner (deployment)
├── requirements.txt
├── setup.py
└── README.md



---

## Machine Learning Workflow
1. **Data Ingestion**
   - Reads raw student dataset
   - Performs train–test split
   - Stores datasets as artifacts

2. **Data Transformation**
   - Handles missing values
   - Encodes categorical features
   - Scales numerical features
   - Saves preprocessing pipeline

3. **Model Training**
   - Trains regression model
   - Evaluates using performance metrics
   - Persists best-performing model

4. **Prediction Pipeline**
   - Loads trained model and preprocessor
   - Generates predictions for new inputs
   - Integrated with Flask frontend

---

## Model Details
- **Problem Type:** Regression
- **Evaluation Metrics:**
  - R² Score
  - Mean Absolute Error (MAE)
- **Model Persistence:** Pickle

---

## Technology Stack
- **Language:** Python
- **ML & Data:** NumPy, Pandas, Scikit-learn
- **Backend:** Flask
- **Frontend:** HTML, CSS
- **Logging:** Python Logging Module
- **Version Control:** Git

---

## Installation & Setup

### Clone the Repository
```bash 
git clone https://github.com/Captain-23/End-to-End-ML-Project
cd MLPROJECT
``` 
### Create and Activate Virtual Environment
```
python -m venv venv
source venv/bin/activate      # macOS / Linux
venv\Scripts\activate         # Windows
```
### Install Dependencies
```
pip install -r requirements.txt
```
### Run the Web Application
```
python app.py
```
### Open your browser and navigate to: 
```
http://localhost:5000
```

---
## Author
**Arnav Alok**
Machine learning and data science enthusiast
