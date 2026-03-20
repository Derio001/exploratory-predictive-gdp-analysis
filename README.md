# 🌍 Global GDP Intelligence: Predictive Analytics & Business Intelligence Dashboard

[![Python](https://img.shields.io/badge/Python-3.8+-blue)](https://www.python.org/)
[![Power BI](https://img.shields.io/badge/Dashboard-Power%20BI-F2C811?logo=powerbi)](https://powerbi.microsoft.com/)
[![Data](https://img.shields.io/badge/Source-World%20Bank-009688)](https://data.worldbank.org/)
[![Models](https://img.shields.io/badge/ML-Random%20Forest%20%7C%20Decision%20Tree-orange)](https://scikit-learn.org/)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)]()

> A full-stack economic intelligence system — integrating 7 World Bank macroeconomic datasets,
> building ML regression models to predict GDP, and delivering a 4-page interactive Power BI
> dashboard for global and country-level economic analysis.

---

## 📊 Dashboard Preview

### Page 1 — GDP Overview
- 🗺️ **World map** — GDP by country (filled choropleth)
- 📈 **GDP trend lines** — Top economies 2000–2024
- 🔢 **KPI cards** — Total global GDP, world population, country count
- 🎛️ **Year range slicer** — filter all visuals dynamically

### Page 2 — Macroeconomic Indicators
- 📉 Exports vs Imports scatter chart
- 🏦 Top countries by FDI Inflows (bar chart)
- 📊 Inflation trends over time (line chart)
- 🌐 Country slicer for filtered analysis

### Page 3 — Model Results
- 🎯 Feature importance ranking (Random Forest)
- 🔵 Actual vs Predicted GDP — Random Forest
- 🔴 Actual vs Predicted GDP — Decision Tree
- 📊 R² score comparison chart

### Page 4 — Country Deep Dive
- 🔍 Country selector with full KPI panel
- 📈 GDP growth trajectory over time
- 📋 Detailed data table with all indicators

---

## 🏗️ Architecture
```
7 World Bank Excel Files (GDP, Exports, Imports, FDI, Inflation, Population, Govt Expenditure)
    ↓
Python Pipeline (pandas) — Melt wide→long, merge on Country+Year, clean missing values
    ↓
EDA — Correlation heatmap, scatter plots, distribution analysis, top economy trends
    ↓
Feature Selection — Random Forest importance ranking
    ↓
ML Models — Decision Tree & Random Forest Regressor (80/20 split)
    ↓
Evaluation — MAE, RMSE, R² | Residual analysis
    ↓
Export — PowerBI_GDP_Main.xlsx + Predictions + Feature Importance
    ↓
Power BI Dashboard — 4 interactive pages
```

---

## 📁 Dataset

- **Source**: [World Bank Open Data](https://data.worldbank.org/)
- **Coverage**: 180+ countries | 2000–2024
- **Indicators integrated**:

| File | Indicator | Role |
|------|-----------|------|
| GDP.xls | GDP (current US$) | **Target variable** |
| Export.xls | Exports of goods & services | Feature |
| Imports.xls | Imports of goods & services | Feature |
| FDI inflows.xls | Foreign Direct Investment net inflows | Feature |
| Inflation.xls | Consumer Price Index | Feature |
| Population.xls | Total population | Feature |
| Goverment_Expenditure.xls | General government expenditure | Feature |

---

## 🤖 Machine Learning Results

| Metric | Decision Tree | Random Forest |
|--------|--------------|---------------|
| MAE | Higher | ✅ Lower |
| RMSE | Higher | ✅ Lower |
| R² Score | Good | ✅ Better |
| **Winner** | | ✅ **Random Forest** |

**Key finding**: Population and Government Expenditure rank as the top GDP predictors globally,
with ensemble methods (Random Forest) significantly outperforming single-tree models by
reducing variance across the high-dimensional cross-country dataset.

---

## 🚀 How to Run

### Python Pipeline
```bash
# Clone
git clone https://github.com/Derio001/exploratory-predictive-gdp-analysis.git
cd exploratory-predictive-gdp-analysis

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl xlrd

# Run the notebook
jupyter notebook Project_Implementation.ipynb
```

### Power BI Dashboard
1. Download [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
2. Open `powerbi_implementation.pbix`
3. If prompted, re-link the data source to your local `PowerBI_GDP_Main.xlsx`

---

## 📁 Project Structure
```
exploratory-predictive-gdp-analysis/
│
├── Project_Implementation.ipynb      # Full Python pipeline (78 cells)
├── powerbi_implementation.pbix       # 4-page Power BI dashboard
│
├── data/
│   ├── Global GDP and Macroeconomic Indicators Dataset/
│   │   ├── GDP.xls
│   │   ├── Export.xls
│   │   ├── Imports.xls
│   │   ├── FDI inflows.xls
│   │   ├── Inflation.xls
│   │   ├── Population.xls
│   │   └── Goverment_Expenditure.xls
│   │
│   ├── Integrated_GDP_Dataset.csv          # Cleaned unified dataset
│   ├── PowerBI_GDP_Main.xlsx               # Main Power BI data source
│   ├── PowerBI_Predictions.csv            # Actual vs predicted GDP
│   └── PowerBI_Feature_Importance.csv     # Feature rankings
│
└── README.md
```

---

## 🔭 Future Work

- [ ] Add Sub-Saharan Africa focused lens (Chad, Niger, Mali, Sudan deep dive)
- [ ] Incorporate conflict/fragility index as a feature for Sahel economies
- [ ] Time-series forecasting (ARIMA / LSTM) for multi-year GDP projection
- [ ] Live World Bank API integration for automatic data refresh
- [ ] Streamlit web app version for browser-based access

---

## 👤 Author

**Mahamat Hanga Derio**
M.Tech Data Science — Christ University, Bangalore
Chadian national | Building economic intelligence tools for Sub-Saharan Africa

📬 Open to collaboration with development banks, economic research institutions & policy organizations
🔗 [GitHub](https://github.com/Derio001) | [LRI Child Health Project →](https://github.com/Derio001/lri-prediction-chad)

---

*Part of a portfolio focused on data-driven economic and public health analysis
for the Lake Chad Basin and Sub-Saharan Africa.*
