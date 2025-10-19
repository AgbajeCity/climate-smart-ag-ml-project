# Predicting Crop Yield with Machine Learning and Smart Farming Data

## Project Mission & Problem Definition

Accurate crop yield prediction is a critical component of climate-smart agriculture, enabling better resource management and enhancing food security. This project addresses this challenge by developing and systematically evaluating a pipeline of machine learning models to predict crop yield (`kg per hectare`) based on a rich set of agricultural sensor and management data.

The mission is to identify a high-performing predictive model and, more importantly, to interpret its decisions to understand the key environmental and operational factors that drive agricultural productivity.

## Dataset

This project uses the **"Smart Farming Sensor Data for Yield Prediction"** dataset, sourced from Kaggle. This dataset was chosen for its direct relevance to the problem and its rich feature set, which includes:
* **Environmental Metrics:** Soil moisture, pH, temperature, rainfall, humidity, and sunlight hours.
* **Management Practices:** Irrigation type, fertilizer type, and pesticide usage.
* **Temporal Data:** Sowing/harvest dates and total growing days.

## Methodology

A comparative analysis was conducted to evaluate the performance of different modeling approaches on this regression task. The pipeline includes:

1.  **Baseline Model:** A `Linear Regression` model to establish a benchmark performance score.
2.  **Ensemble Learning Model:** A `Random Forest Regressor` to capture complex, non-linear relationships in the data.
3.  **Systematic Optimization:** The Random Forest was optimized using `GridSearchCV` to find the best hyperparameters, demonstrating a rigorous approach to model improvement.
4.  **Deep Learning Model:** A `Multi-Layer Perceptron (MLP)` built with TensorFlow/Keras to compare a deep learning approach against traditional methods.

The preprocessing pipeline includes feature engineering, one-hot encoding for categorical variables, and feature scaling (`StandardScaler`) for the neural network.

## Key Results

The systematically **Tuned Random Forest Regressor** was the top-performing model, achieving an **R-squared (R²) of 0.91** on the unseen test data.

Feature importance analysis revealed that the **top 3 predictors of crop yield** were:
1.  `total_days` (the length of the growing season)
2.  `rainfall_mm`
3.  `pesticide_usage_ml`

## Repository Contents

* `Climate_Smart_Yield_Prediction.ipynb`: The main Google Colab notebook containing all data preprocessing, model training, evaluation, and analysis code.
* `Smart_Farming_Crop_Yield_2024.csv`: The dataset used for the project.

## Instructions for Reproducibility

To run this project and reproduce the results:
1.  Ensure you have both the `.ipynb` and `.csv` files.
2.  Upload both files to a Google Colab session.
3.  Execute the cells in the notebook sequentially from top to bottom. All required libraries and dependencies are handled within the notebook.
