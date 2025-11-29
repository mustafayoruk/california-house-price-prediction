# california-house-price-prediction
Deep Learning Regression Model with TensorFlow

#  California Housing Price Prediction (Deep Learning Regression)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Status](https://img.shields.io/badge/Status-Success-green)

##  Project Overview
This project applies **Deep Learning** techniques to predict median house values in California districts based on the 1990 Census data. Unlike classification tasks, this is a **regression problem** where the model estimates a continuous numerical value ($).

As a Statistics student, my focus was on **data integrity**, **statistical preprocessing**, and increasing the **R-Squared ($R^2$)** score through architecture optimization.

##  Dataset
The dataset consists of 20,640 observations.
* **Input Features:** Longitude, Latitude, Housing Median Age, Total Rooms, Total Bedrooms, Population, Households, Median Income, Ocean Proximity.
* **Target Variable:** Median House Value.

##  Methodology & Improvements

### 1. Data Preprocessing (Statistical Approach)
* **Outlier Removal:** Houses with a value of **$500,001** (capped limit) were identified as outliers and removed to prevent skewing the model.
* **Imputation:** Missing values in the `total_bedrooms` column were filled with the mean.
* **Encoding:** Categorical feature `ocean_proximity` was converted using **One-Hot Encoding**.
* **Scaling:** Applied `StandardScaler` (Z-Score normalization) to ensure feature uniformity.

### 2. Neural Network Architecture
A sequential ANN model was built using TensorFlow/Keras:
* **Hidden Layers:** 3 Dense layers (128 -> 64 -> 32 neurons) with **ReLU** activation to capture non-linear patterns.
* **Output Layer:** 1 Neuron with **Linear** activation (standard for regression).
* **Optimizer:** Adam with a custom learning rate (0.001) for stable convergence.
* **Loss Function:** Mean Squared Error (MSE).

##  Results (Model V2.0)
After cleaning outliers and deepening the network, the model achieved:

* **R-Squared ($R^2$):** ~0.72
* **Mean Absolute Error (MAE):** ~$36,000
* **Conclusion:** The model explains approximately **72%** of the variance in house prices, providing a reliable baseline for price estimation.

##  How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/mustafayoruk/california-housing-price-prediction.git](https://github.com/mustafayoruk/california-housing-price-prediction.git)
    ```
2.  Install requirements:
    ```bash
    pip install pandas tensorflow scikit-learn matplotlib seaborn
    ```
3.  Run the Jupyter Notebook ensuring `housing.csv` is in the same directory.

---
**Author:** [Mustafa YÖRÜK]  
*Statistics Student @ Hacettepe University*
