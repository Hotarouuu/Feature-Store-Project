# Data Science Academy Project - Feature Store Project

## Introduction

In this small project, I'm creating a full Machine Learning Pipeline focusing on feature store, feature engineering and training. We are not creating a prediction script this time.
This small project was developed in the "Formação Machine Learning 4.0" by Data Science Academy. All credit goes to them.

---

## Table of Contents

- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)

  * [1. Data Exploration and Processing](#1-data-exploration-and-processing)
  * [2. Feature Engineering](#2-feature-engineering)
  * [3. Feature Store](#3-feature-store)
  * [4. Modeling](#4-modeling)
  * [5. Model persistence and Training ](#5-model-persistence-and-training)
  * [6. Pipeline Execution](#6-pipeline-execution)
* [Conclusion](#conclusion)

---

## Technologies Used

- Scikit-Learn
- Numpy
- UV
- joblib
- Pandas
- Seaborn

---

## Project Structure

    ├── artifacts
    ├── feature_store/
    ├── pipeline_runs/
    ├── src/
    │   ├── data/
    │   │   ├── feature_store.py
    │   │   └── explore_data.py
    │   └── model/
    │       ├── train.py
    │       └── save.py
    ├── pyproject.toml
    ├── main.py
    ├── uv.lock

---

## 1. Data Exploration and Processing

In this phase, descriptive statistical analyses, evaluation of the distribution of variables, and general inspection of data quality are performed.

The objective of this phase is to understand the behavior of the variables before training the model, identify potential problems, and generate initial insights that aid in the interpretation of the results.

---

## 2. Feature Engineering

This step includes data processing, creation of new variables, structural adjustments, and consolidation of the final dataset.

The result of this phase is a DataFrame ready to be used in model training.

---

## 3. Feature Store

This step includes data processing, creation of new variables, structural adjustments, and consolidation of the final dataset.

The result of this phase is a DataFrame ready to be used in model training.

---

## 4. Modeling

The modeling stage is responsible for training and evaluating the Machine Learning algorithm. The pipeline uses the RandomForestClassifier algorithm.

This phase involves separating training and test data, training the model, generating predictions, and calculating performance metrics, including accuracy and classification reporting.


---

## 5. Model persistence and Training 

After training, the model is saved in the `pipeline_runs/` directory in the `.joblib` format. Additionally, predictions are stored in a CSV file, along with the actual values ​​from the test set.

The pipeline also generates a JSON file called `pipeline_run_info.json`, containing important run information such as the type of model used, paths to saved artifacts, and metrics obtained.


---

## 6. Pipeline Execution

All the orchestration of the steps is performed by the `main.py` file. It is responsible for:

- Creating necessary directories
- Executing the creation of the Feature Store
- Performing exploratory analysis
- Training the model
- Saving artifacts
- Logging execution information

To run the project, simply run:

python main.py

Or, using uv:

uv run python main.py

---

## Conclusion

The main objective of this project is to demonstrate the construction of a structured Machine Learning pipeline focusing on:

- Modular code organization
- Feature engineering
- Model persistence
- Execution traceability
- Reproducibility



