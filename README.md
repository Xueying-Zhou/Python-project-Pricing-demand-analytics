# 🚖 Pricing & Demand Analytics

🔗 **Live Report:**  
[View Interactive Analysis](https://xueying-zhou.github.io/Python-project-Pricing-demand-analytics/)

Applied econometric modeling and clustering-based demand estimation in Python.

---

## 📌 Overview

This project analyzes:

- **Ride-hailing pricing structure** (UberX vs Lyft)  
- **Demand estimation under stockout conditions** (Flash sale case)

The objective is to understand pricing drivers and recover hidden demand using regression and clustering techniques.

---

## 🚗 Part I — Ride-Hailing Price Modeling

### Objective

Model ride price as a function of:

- Distance  
- Origin (source)  
- Time of day (hour)

---

### Models Implemented

- One-way ANOVA  
- Basic OLS: `Price ~ Distance`  
- Dummy variable model  
- Interaction model  
- Full model (distance + dummies + interactions)

---

### Key Insights

- Distance alone underfits pricing behavior.  
- Time and location significantly shift price levels.  
- Interaction terms allow slope variation across time and origin.  
- The full model achieves the best overall fit (Adj-R² & AIC).  
- Lyft exhibits stronger distance sensitivity than UberX.

---

## 🛍 Part II — Flash Sale Demand Estimation

### Objective

Estimate true demand for sold-out items using clustering.

---

### Methodology

1. Construct hourly cumulative sales fractions  
2. Cluster non-stockout items (k = 2, 4)  
3. Assign stockout items to nearest cluster  
4. Estimate lost demand  

---

### Findings

- k = 4 captures richer temporal demand structures.  
- Estimated demand differs by only ~1–2% across k values.  
- Clustering effectively recovers hidden sales potential.

---

## 🛠 Methods & Tools

- Python  
- NumPy  
- Pandas  
- SciPy  
- Scikit-learn  
- Matplotlib  

Custom OLS was implemented from scratch using NumPy to compute:

- R²  
- Adjusted R²  
- AIC  

---

## 📂 Repository Structure

```
pricing-demand-analytics/
│
├── data/
├── notebooks/
│   └── analysis_walkthrough.ipynb
├── reports/
│   └── analysis_report.html
└── README.md
```

---

## 💡 Skills Demonstrated

- Econometric modeling  
- Dummy & interaction encoding  
- Model comparison & diagnostics  
- K-Means clustering  
- Demand recovery under missing data  
- Business interpretation of statistical results  

---

## 👩‍💻 Author

**Aria Zhou**  
Master of Management Sciences (Data Analytics)  
University of Waterloo
