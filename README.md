# CFEM: Composite Forecasting Evaluation Metric for Time Series Models

🎓 Bachelor's Thesis Project – BSc in Computer Science  
📍 University of Venice – Academic Year 2023/2024  
👨‍💻 Author: Alessandro Conte  
📘 Advisor: Prof. Ilaria Prosdocimi  

---

## 📝 Project Overview

This repository contains the implementation and explanation of a **composite metric (CFEM)** for evaluating forecasting models on time series data. The metric combines four traditional error measures (RMSE, MAE, MAPE, MASE), addressing their individual limitations and enhancing comparability across different datasets and models.

The work was developed as part of a thesis internship at **Humco**, and includes the design, implementation, and testing of the metric on real datasets using models like **ARIMA, SARIMA, Holt-Winters, and Prophet**.

📄 [Read the full thesis (PDF, Italian)](./thesis.pdf)

---

## 📊 Main Objectives

- Design a unified metric that balances the strengths and weaknesses of standard error measures.
- Normalize and weigh the metrics based on data characteristics (trend, seasonality, outliers).
- Evaluate the metric on real-world datasets with different models.
- Discuss its robustness and future improvements.

---

## 📂 Repository Structure

📁 cfem-time-series-evaluation/
├── README.md <- You are here
├── thesis.pdf <- Full thesis document (Italian)
├── notebook/
│ └── cfem_notebook.ipynb <- Google Colab notebook with full implementation
├── src/
│ └── utils.py <- Optional: utility functions
├── data/
│ └── sample_data.csv <- Optional: if publicly shareable
└── requirements.txt <- Optional: dependencies for running the code

---

## 🔧 Models and Tools

- Forecasting Models: ARIMA, SARIMA, Holt-Winters, Prophet
- Libraries: `pandas`, `numpy`, `matplotlib`, `statsmodels`, `fbprophet`, `scikit-learn`
- Validation: Expanding Window Cross-Validation
- Notebook: [Google Colab Compatible]

---

## 📈 CFEM Formula

The **Composite Forecasting Evaluation Metric (CFEM)** is defined as:

```math
CFEM = (Σ wᵢ * mᵢ) / Σ wᵢ
```

Where:

* `mᵢ` = normalized value of each error metric (Min-Max normalization)
* `wᵢ` = weight computed based on:

  * Seasonality strength (via STL decomposition)
  * Median or mean error across CV folds
  * Metric-specific significance (depending on data characteristics)

---

## 📌 Future Work

* Improve the robustness of the weight computation
* Test the metric on more complex datasets
* Package CFEM as a reusable Python module

---

## 📬 Contact

Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/alessandro-conte-ds/) or reach out for collaboration.

````

