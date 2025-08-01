# Room Occupancy Prediction using Machine Learning

A machine learning project to predict room occupancy based on real-time environmental sensor data. This model can be used to build smart, energy-efficient systems for homes and offices.

---

## Overview

This project explores the use of machine learning to determine whether a room is occupied or empty. By analyzing data from various environmental sensors—specifically Temperature, Humidity, and CO2 levels—we can build a highly accurate classification model. The core idea is that human presence significantly alters these environmental variables, creating a detectable pattern.

This repository contains the Jupyter notebooks, datasets, and analysis required to replicate the findings. The final model, a **Random Forest Classifier**, achieves an accuracy of **98.6%** on the test data.

---

## Features

* **High-Accuracy Prediction:** Achieves 98.6% accuracy in classifying room occupancy.
* **Comprehensive EDA:** Includes detailed Exploratory Data Analysis with visualizations to understand data trends.
* **Model Comparison:** Implements and evaluates six different classification algorithms to find the optimal solution.
* **Reproducible Workflow:** Contains all necessary code and data for others to run the analysis.

---

## Dataset

The project utilizes two primary datasets:

1.  `data_27092022.csv`: The main dataset used for training and testing the models. It contains 7,899 records.
2.  `for_correlation.csv`: A supplementary dataset used for deeper exploratory analysis, which also includes a `Lux` (light level) feature.

The key features used for prediction are:

* `Temperature` (°C)
* `Humidity` (%)
* `CO2` (ppm)
* `Occupancy status` (0 for Not Occupied, 1 for Occupied) - *Target Variable*

---

## Methodology

The project followed a standard machine learning workflow:

1.  **Data Preprocessing:** The raw data was loaded, cleaned of any irrelevant information, and prepared for analysis. A key step involved creating a unified `exact_time` column from separate date and time fields for accurate time-series analysis.

2.  **Exploratory Data Analysis (EDA):** A deep dive into the dataset was performed to uncover patterns. Visual analysis was crucial here. Time-series plots showed clear shifts in sensor readings that corresponded with changes in occupancy status. Furthermore, a correlation heatmap revealed the strong relationships between variables, particularly how CO2 levels rise significantly with human presence. This analysis confirmed that the chosen features were highly relevant for prediction.

3.  **Model Training & Evaluation:** The problem was treated as a binary classification task. Six different models were trained and then evaluated based on their accuracy on a held-out test set.

---

## Results

The performance of the different models was compared to identify the most effective one. The Random Forest classifier slightly outperformed the others.

| Model                  | Accuracy on Test Set |
| ---------------------- | -------------------- |
| **Random Forest** | **98.60%** |
| Decision Tree          | 98.48%               |
| K-Nearest Neighbors    | 98.41%               |
| Support Vector Machine | 98.22%               |
| Logistic Regression    | 97.97%               |
| Naive Bayes            | 97.97%               |

The results show that the environmental features are highly predictive of room occupancy.

---

## How to Run This Project

To run this project on a local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    ```

2.  **Install the required libraries:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```

3.  **Navigate to the project directory and run Jupyter Notebook:**
    ```bash
    cd your-repository-name
    jupyter notebook
    ```

4.  Open the `code_occupancy_iit_kgp-updated.ipynb` file to see the main analysis and model training.
