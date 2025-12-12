# Car of the Year: Predicting Car Demand with Linear Regression

## Project Overview
This project analyzes used car market data to understand **what factors influence car demand** and to identify **which car models are expected to be the most in demand in 2025**.

Because the dataset does not include literal sales volume, we use **resale price as a proxy for demand**, based on the assumption that cars with higher sustained resale value reflect stronger buyer preference.

Using **Linear Regression**, we model how vehicle characteristics such as mileage, age, brand, engine size, and fuel type affect demand and rank car models accordingly.

---

## Research Question
**Which car model is expected to have the highest demand in 2025, and what features drive that demand?**

---

## Dataset
- **Source:** Kaggle – Global Car Sales Analysis  
- **Link:** https://www.kaggle.com/datasets/mubeenshehzadi/global-car-sales-analysis  
- **Description:**  
  The dataset contains used car listings with the following key attributes:
  - Manufacturer  
  - Model  
  - Engine size  
  - Fuel type  
  - Year of manufacture  
  - Mileage  
  - Resale price  

---

## Methodology
1. **Data Cleaning & Preprocessing**
   - Removed rows with missing values in critical columns
   - Converted numeric fields to appropriate types
   - One-hot encoded categorical variables (manufacturer, fuel type)

2. **Feature Engineering**
   - Selected mileage, year of manufacture, engine size, manufacturer, and fuel type as input features
   - Created a combined `car_id` (manufacturer + model) for ranking purposes

3. **Modeling**
   - Used **Linear Regression** to predict resale price
   - Interpreted predicted price as a **demand score**
   - Evaluated the model using MAE, RMSE, and R²

4. **Demand Ranking**
   - Averaged predicted demand scores across listings for each car model
   - Ranked models to identify the most in-demand vehicles

---

## Key Results
- The model achieved an **R² of 0.687**, explaining approximately **69% of the variation in resale price**
- **Mileage and year of manufacture** were the strongest predictors of demand
- **Brand reputation and fuel type** also played significant roles
- The **BMW M5** emerged as the most in-demand car model for 2025 based on predicted demand scores

---

## Files in This Repository
- `car_sales_data.csv` – Dataset used for analysis  
- `TripleTroubleFinalCode.ipynb` – Complete analysis, modeling, and results  
- `README.md` – Project overview and instructions  

---

## How to Run the Code
1. Clone this repository
2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
3. Open and run the jupyter notebook

---

## Authors
- Oscar Alvarado
- Joseph Gardner
- Advik Katiyar
