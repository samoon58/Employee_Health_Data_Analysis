# Employee_Health_Data_Analysis

# Employee Health & Workplace Analytics

This project cleans, processes, and analyzes employee demographics alongside health and wellness metrics. Using Python, Pandas, and NumPy, the pipeline transforms raw data into structured insights regarding workplace productivity, stress levels, work-life balance, and departmental demographics.

---

## 📌 Project Overview

The main objective of this repository is to combine disparate employee datasets (demographics and health metrics) to evaluate key operational and wellness factors:
* Data Cleaning & Standardization: Handling duplicates, string formatting, date/time extraction, and null value imputation.
* Statistical Aggregation: Metrics for age, stress levels, work hours, sleep patterns, and daily activity.
* Data Merging & Grouping: Department-level distributions, productivity scores, and gender breakdowns.
* Correlation Analysis: Statistical relationships between work hours, sleep hours, and overall productivity scores.

---

## 🛠️ Data Pipeline & Key Features

### 1. Data Ingestion & Cleaning
* Deduplication: Removes duplicate entries across both `Employee_Details.csv` and `Employee_Health.csv`.
* String Normalization: Strips unwanted characters (`/123_.`) from employee names and standardizes department names to lowercase.
* Handling Missing Data: Imputes missing department values with `'Unknown department'`.
* Date & Time Extraction: Parses datetime values in `LastLogin` to separate `Last_Login_Date` and `Last_Login_Time`.
* Feature Transformation: Maps binary categories (e.g., converting `SmokingStatus` into numeric values: `Smoker = 1`, `Non-Smoker = 0`).

### 2. Statistical Analysis & Metrics
Calculates core statistical measures across health and demographic metrics:
* Mean: Average employee age.
* Median: Work hours median (`np.nanmedian`).
* Extremes: Minimum sleep hours (`np.nanmin`) and maximum step count (`np.nanmax`).

### 3. Data Merging & Department Analysis
* Outer and Inner Joins: Integrates `Employee_Details` and `Employee_Health` using key identifiers (`Name` and `EmployeeID`).
* Departmental Grouping: Calculates gender distributions per department and average productivity scores.
* Correlation Matrix: Computes linear correlation between `WorkHours`, `SleepHours`, and `ProductivityScore`.

---

# Employee Health & Workplace Analytics

This project cleans, processes, and analyzes employee demographics alongside health and wellness metrics. Using Python, Pandas, and NumPy, the pipeline transforms raw data into structured insights regarding workplace productivity, stress levels, work-life balance, and departmental demographics.

---

## 📁 Repository Structure

```text
.
├── Input/
│   ├── Employee_Details.csv
│   └── Employee_Health.csv
├── faisal_python_project_bada_feb2026.py
├── Faisal_Python_project_BADA_FEB2026.ipynb
└── README.md


## 📊 Dataset Structure

The project processes two primary CSV datasets:

1. Employee_Details.csv
   * `EmployeeID` — Unique employee identification key
   * `Name` — Employee full name
   * `Age` — Employee age
   * `Department` — Department assignment
   * `LastLogin` — Timestamp of last system activity

2. Employee_Health.csv
   * `EmployeeID` / `Name` — Key identifiers for merging
   * `SmokingStatus` — Categorical status (`Smoker` / `Non-Smoker`)
   * `WorkHours` — Weekly or daily work hours
   * `SleepHours` — Average hours of sleep
   * `StepCount` — Daily physical activity (steps)
   * `ProductivityScore` — Performance/productivity evaluation score

---

## 🚀 Getting Started

### Prerequisites
Make sure you have Python installed along with the required libraries:

```bash
pip install pandas numpy matplotlib seaborn
