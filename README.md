# 🚗 Uber Data Analysis

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/Seaborn-Visualization-4C72B0" />
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white" />
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen" />
</p>

## 📌 Overview

This project performs a comprehensive **Exploratory Data Analysis (EDA)** on Uber ride request data to uncover demand patterns, peak usage hours, and trip behavior. The insights derived can help Uber optimize driver allocation, reduce cancellations, and improve customer satisfaction.

---

## 📂 Dataset

| Feature | Description |
|---|---|
| `Request id` | Unique identifier for each ride request |
| `Pickup point` | Origin of the ride (City / Airport) |
| `Status` | Outcome of the request (Trip Completed / No Cars Available / Cancelled) |
| `Request timestamp` | Date and time of the request |
| `Drop timestamp` | Date and time of the trip completion |

---

## 🔍 Project Workflow

### 1. Data Preprocessing
- Loaded the dataset using **Pandas**
- Detected and handled **missing values** (`isnull().sum()`)
- Converted `Request timestamp` and `Drop timestamp` columns from `object` to `datetime` format
- Engineered new time-based features:
  - `HOUR` — Hour of the day
  - `DAY` — Day of the month
  - `MONTH` — Month
  - `WEEKDAY` — Day name (Monday, Tuesday, ...)
  - `DAY_OF_WEEK` — Day number (0–6)

### 2. Univariate Analysis
Analyzed the distribution of individual variables:
- **Categorical:** Bar charts and pie charts for `WEEKDAY`, `Pickup point`, and `Status`
- **Numerical:** KDE plots, boxplots, boxenplots, violin plots, distribution plots, and histograms for `HOUR` and `MONTH`

### 3. Bivariate Analysis
- Scatter plots between `Request timestamp` and `HOUR`
- Linear model (lmplot) between `DAY` and `HOUR`
- **Correlation heatmap** to explore relationships between numerical features

### 4. Countplot Analysis
- Request count by hour, segmented by **Status** and **Pickup point**
- Request count by month, day, and weekday

### 5. GroupBy Analysis
- Average metrics grouped by `WEEKDAY` and `Pickup point`

---

## 📊 Key Insights

- 🕐 **Peak hours** occur in the early morning (airport rush) and late evening (city demand)
- 🏙️ **City pickups** significantly outnumber airport pickups
- ❌ A notable proportion of requests result in **"No Cars Available"** — indicating supply gaps during peak times
- 📅 Demand is relatively consistent across weekdays with slight weekend variation

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| Python 3.x | Core programming language |
| Pandas | Data loading, cleaning, and manipulation |
| NumPy | Numerical operations |
| Matplotlib | Static visualizations |
| Seaborn | Statistical data visualization |
| Datetime / Calendar | Timestamp parsing and feature engineering |
| Jupyter Notebook | Interactive development environment |

---

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Run the Notebook
```bash
git clone https://github.com/MehmetErtass/Uber_Data_Analysis.git
cd Uber_Data_Analysis
jupyter notebook Uber-Python.ipynb
```

---

## 📁 Project Structure

```
Uber_Data_Analysis/
│
├── Uber-Python.ipynb          # Main analysis notebook
├── Uber Request Data.csv      # Dataset
└── README.md                  # Project documentation
```

---

## 👨‍💻 Author

**Mehmet Ertaş**  
[![GitHub](https://img.shields.io/badge/GitHub-MehmetErtass-181717?logo=github)](https://github.com/MehmetErtass)
