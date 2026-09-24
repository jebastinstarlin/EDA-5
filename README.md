# 🏥 Healthcare Data Analysis

## 📌 Project Overview

This project analyzes a healthcare dataset using **Python and Pandas**. The notebook performs data loading, dataset inspection, data cleaning, date conversion, descriptive statistics, and exploratory analysis of patient and billing information.

---

## 📊 Dataset

The project uses the following file:

```text
healthcare_raw.csv
```

The dataset contains **500 rows and 9 columns**.

### 📋 Columns

| Column              | Description                                              |
| ------------------- | -------------------------------------------------------- |
| `Patient_ID`        | Unique patient identifier                                |
| `Gender`            | Patient gender                                           |
| `Age`               | Patient age                                              |
| `Medical_Condition` | Recorded medical condition                               |
| `Admission_Date`    | Patient admission date                                   |
| `Admission_Type`    | Type of admission, such as Routine, Urgent, or Emergency |
| `Medical_Code`      | Medical/ICD10 code                                       |
| `Billing_Amount`    | Patient billing amount                                   |
| `Discharge_Date`    | Patient discharge date                                   |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Google Colab / Jupyter Notebook**

---

# 🔍 Project Workflow

## 1. Import Libraries

The project uses NumPy, Pandas, Matplotlib, and Seaborn for data processing, analysis, and visualization.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

---

## 2. Load the Dataset

The healthcare CSV file is loaded into a Pandas DataFrame:

```python
df = pd.read_csv("/content/healthcare_raw.csv")
```

The dataset is stored in the DataFrame `df`.

---

## 3. Explore the Dataset

The notebook examines the basic structure and contents of the dataset.

The following aspects are checked:

* Number of rows and columns
* Column names
* Dataset contents
* Data types
* Descriptive statistics

The dataset contains **500 records and 9 attributes**.

---

## 4. Missing Value Handling

The `Medical_Code` column is checked for missing values.

Missing values, if present, are replaced with `"Unknown"`:

```python
df["Medical_Code"] = df["Medical_Code"].fillna("Unknown")
```

The notebook then verifies that no missing values remain in this column.

---

## 5. Date Conversion

The `Admission_Date` and `Discharge_Date` columns are converted from text values into Pandas datetime format.

```python
df["Admission_Date"] = pd.to_datetime(df["Admission_Date"])
df["Discharge_Date"] = pd.to_datetime(df["Discharge_Date"])
```

This allows the date columns to be used for date-based analysis and calculations.

---

## 6. Statistical Analysis

Descriptive statistics are generated for numerical columns such as:

* `Age`
* `Billing_Amount`

Based on the dataset analysis:

* The average age is approximately **50.11 years**.
* The average billing amount is approximately **7249.00**.

---

# 📈 Key Dataset Information

| Attribute                  |    Value |
| -------------------------- | -------: |
| **Number of records**      |      500 |
| **Number of columns**      |        9 |
| **Average age**            |    50.11 |
| **Minimum age**            |       22 |
| **Maximum age**            |       78 |
| **Average billing amount** |  7249.00 |
| **Minimum billing amount** |  2300.00 |
| **Maximum billing amount** | 14200.00 |

---

# 🎯 Purpose of the Project

The main purpose of this project is to practice **healthcare data analysis using Python**.

The project demonstrates how to:

* Load a healthcare dataset
* Understand the dataset structure
* Inspect data types and records
* Check and handle missing values
* Convert date columns
* Generate descriptive statistics
* Analyze basic patient and billing information

---

# 🚀 How to Run

## Using Google Colab

1. Open `Health_Care.ipynb` in Google Colab.
2. Upload `healthcare_raw.csv` to the working environment.
3. Make sure the dataset is available at:

```text
/content/healthcare_raw.csv
```

4. Run the notebook cells from top to bottom.
5. Review the data inspection, cleaning, and analysis outputs.

---

## Using Jupyter Notebook

Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Health_Care.ipynb
```

Place `healthcare_raw.csv` in the required location and run all notebook cells.

---

# 📁 Project Files

```text
Healthcare-Data-Analysis/
│
├── Health_Care.ipynb
├── healthcare_raw.csv
└── README.md
```

---

# 📝 Conclusion

This project provides a basic workflow for analyzing healthcare records using **Python and Pandas**.

It focuses on:

* Data understanding
* Data cleaning
* Missing value handling
* Date conversion
* Descriptive statistics
* Basic patient and billing analysis

The project can be further extended with additional **visualizations, patient demographics analysis, admission trends, billing analysis, and deeper healthcare data exploration**.
