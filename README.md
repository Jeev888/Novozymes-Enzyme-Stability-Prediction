# Bioinformatics - Novozymes Enzyme Stability Prediction

This repository contains the final submission for the Tokihub internship assignment, which focuses on the **Novozymes Enzyme Stability Prediction** problem. The goal of this project is to demonstrate an end-to-end data science pipeline for a challenging bioinformatics problem involving large, real-world data.

---

## 1. Project Summary

This project implements a machine learning workflow to predict the binding affinity of a molecule to a protein target. The core challenges of this assignment were the **massive size of the dataset (~54 GB)** and the **severe class imbalance** in the target variable.

To address these challenges, the following steps were taken:

* **Memory-Efficient Data Handling:** The full `train.csv` dataset was analyzed in manageable chunks to understand the target variable's distribution without exceeding memory limitations.
* **Stratified Subset Creation:** A smaller, **balanced subset** of the data was created by collecting an equal number of binding and non-binding examples. This is a critical step to ensure a simple model can learn effectively from all classes.
* **Data Cleaning & Preprocessing:** The subset was cleaned by removing duplicate molecules to prevent data leakage and ensure model generalization. Categorical features (SMILES strings and protein names) were then converted into a numerical format using one-hot encoding.
* **Modeling & Evaluation:** A **Logistic Regression model** was chosen as a simple, interpretable baseline classifier. The model was trained and evaluated, demonstrating a robust end-to-end pipeline. The high accuracy and strong precision and recall scores were a direct result of the balanced dataset and sound preprocessing.
* **Research Summary:** A detailed write-up on current State-of-the-Art (SOTA) techniques in molecular binding prediction is included in the notebook's markdown cells, as required by the assignment.

This project demonstrates a practical and logical approach to tackling a complex, real-world bioinformatics problem within resource constraints, which is a key skill for a computational biologist and AI engineer.

---

## 2. Deliverables and Dataset Information

The following files are included in this repository to fulfill the assignment requirements:

* **Code Submission:** The Jupyter Notebook (`tokihub_final.ipynb`) contains all the code, detailed explanations, and visualizations for each step of the data science pipeline.
* **Research Summary:** The research write-up on SOTA techniques is included as a markdown section within the notebook.
* **Dataset:** The dataset used for this project is the **Novozymes Enzyme Stability Prediction** dataset.

**Dataset Link:** `https://www.kaggle.com/competitions/leash-BELKA/data`

**Note:** This work was performed using a Kaggle Notebook, which provides access to the large dataset without requiring a local download.
