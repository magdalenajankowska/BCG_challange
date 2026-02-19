# 🌾 BCG Challenge — Use Case 1: Barley Yield & Climate Variability Analysis

**University Project | BCG University Collaboration**

This use case analyzes the impact of climate variables on barley yield across French departments.
It combines agricultural data, climate indicators, and machine learning models to:

* Predict barley yields
* Estimate yield variability
* Simulate climate stress scenarios
* Calculate future production under different assumptions
* Visualize spatial differences across France

The main analysis is implemented in `model2.ipynb`.

---

# 📌 Use Case Objectives

* Build a predictive model for barley yield using historical climate data
* Evaluate model performance using a time-based train/test split
* Estimate 2025 yields across French departments
* Simulate climate stress scenarios (e.g., +2°C summer temperature)
* Calculate department-level and total production
* Visualize yield variability geographically

---

# 🧠 Methodology

## 1️⃣ Data Preparation

* Monthly and seasonal climate indicators:

  * Mean, max, min temperature
  * Precipitation (sum, mean, max, min)
* Growing degree days (GDD)
* Heat days and dry days
* Department encoding (one-hot encoding)
* Temporal split:

---

## 2️⃣ Modeling

* CatBoost model for yield prediction
* Lasso Regression for yield prediction
* Time-based validation (not random split)
* Scenario simulations for stress testing

---

## 3️⃣ Climate Stress Testing

Example scenario:

* +2°C increase in summer maximum temperature
* Reduced spring precipitation

Impact is calculated as:

Average Yield Drop = Baseline Prediction − Stress Scenario Prediction

This allows quantification of climate vulnerability.

---

## 4️⃣ Production Estimation (2025)

For each department:

Production = Average Yield (2025, across scenarios) × Area (2018)

Then total national production is calculated by summing department-level production.

---

# 📊 Outputs

The notebook generates:

* Model performance metrics
* Yield prediction map
* Yield variability map
* Climate resiliance map
* 2025 production estimates
* Total projected production

---

# 📂 Repository Structure

```
BCG_challange/
│
├── model2.ipynb        # Main modeling notebook
├── data/               # Input datasets
└── README.md           # Project documentation
```

---

# 🛠 Technologies Used

* Python 3.11
* pandas
* numpy
* scikit-learn
* matplotlib
* geopandas
* Jupyter Notebook

---

