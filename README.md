# 🛢️ OilyGiant — Optimal Oil Well Location Prediction

## 📘 Overview
This project helps **OilyGiant Mining Company** identify the most profitable region for developing new oil wells.  
Using geological data from three regions, a **Linear Regression** model predicts oil reserves, estimates potential profits, and evaluates investment risks using **bootstrapping**.

---

## 🚀 Project Steps

### 1. Data Preparation
- Load and preprocess geological data for three regions:  
  - `geo_data_0.csv`  
  - `geo_data_1.csv`  
  - `geo_data_2.csv`
- Each dataset contains:
  - `id` — unique oil well identifier  
  - `f0`, `f1`, `f2` — geological features  
  - `product` — actual oil reserve volume (thousand barrels)

---

### 2. Model Training
For each region:
- Split the data into **75% training** and **25% validation** sets.  
- Train a **Linear Regression** model to predict oil reserves.  
- Evaluate model performance using **RMSE** and the average predicted reserve volume.

---

### 3. Profit Calculation
- Budget: **$100 million** for **200 wells**.  
- Revenue per thousand barrels: **$4,500**.  
- Select the **top 200 wells** with the highest predicted reserves.  
- Calculate the total profit for each region.

---

### 4. Risk Assessment
- Apply **Bootstrapping (1,000 samples)** to estimate:
  - Average profit  
  - 95% confidence interval  
  - Probability of loss (negative profit)
- Only regions with a **risk of loss < 2.5%** are considered.  
- Choose the region with the **highest mean profit** and acceptable risk.

---

## 🛠️ Tools & Libraries
- **Python**  
- **Pandas**  
- **NumPy**  
- **Scikit-learn**  
- **Matplotlib**  
- **Seaborn**

---

## 📈 Outcome
The project delivers a **data-driven recommendation** for selecting the optimal region to develop new oil wells — maximizing **profitability** while minimizing **financial risk**.

---

## 📁 Data
| File | Description |
|------|--------------|
| `geo_data_0.csv` | Geological data for region 0 |
| `geo_data_1.csv` | Geological data for region 1 |
| `geo_data_2.csv` | Geological data for region 2 |

> ⚠️ *All datasets are synthetic and provided for educational and analytical purposes.*

---

## 🧮 Key Assumptions
- Only **Linear Regression** is used for predictions.  
- Each exploration studies **500 points**, and the **best 200** are developed.  
- Development budget: **$100 million**.  
- Revenue per unit (thousand barrels): **$4,500**.  

---

## 📊 Results
- Predicted oil reserves and RMSE per region.  
- Estimated profits with confidence intervals.  
- Final recommendation for the **most profitable, lowest-risk region**.

---

## 🏁 Conclusion
This analysis enables OilyGiant to make a **data-informed investment decision**, identifying the region with the **highest expected profit** and **minimal financial risk**.
