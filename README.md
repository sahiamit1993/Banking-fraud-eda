# 🏦 Banking Credit Card Fraud Detection — PySpark EDA Project

## 📌 Project Overview

This project performs an end-to-end Exploratory Data Analysis (EDA) on a large-scale banking credit card transaction dataset using PySpark.

The objective is to identify fraudulent transaction patterns, analyze customer transaction behavior, and demonstrate scalable big data analytics using Apache Spark.

This project is designed for:

* Data Analyst Portfolio
* Data Engineering Portfolio
* PySpark Practice
* Big Data Analytics Projects
* GitHub Showcase Projects
* Interview Preparation

---

# 🚀 Tech Stack

| Technology       | Purpose                     |
| ---------------- | --------------------------- |
| Python           | Programming Language        |
| PySpark          | Distributed Data Processing |
| Spark SQL        | SQL-based Analytics         |
| Pandas           | Small-scale transformations |
| Matplotlib       | Data Visualization          |
| Seaborn          | Statistical Visualization   |
| Plotly           | Interactive Visualization   |
| Jupyter Notebook | Development Environment     |
| Git & GitHub     | Version Control             |

---

# 📊 Dataset Information

### Dataset

Credit Card Fraud Detection Dataset

### Source

[https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

### Dataset Details

| Feature                | Value             |
| ---------------------- | ----------------- |
| Total Rows             | 284,807           |
| Total Columns          | 31                |
| Fraud Transactions     | 492               |
| Non-Fraud Transactions | 284,315           |
| File Size              | ~143 MB           |
| Domain                 | Banking & Finance |

---

# ⚙️ PySpark Configuration

## SparkSession Configuration

```python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("Banking Fraud EDA") \
    .config("spark.executor.memory", "4g") \
    .config("spark.driver.memory", "4g") \
    .config("spark.sql.shuffle.partitions", "8") \
    .getOrCreate()
```

---

# 📥 Data Ingestion

The project reads raw CSV transaction data using PySpark and converts it into Parquet format for optimized processing.

### Steps Performed

* Load CSV file
* Infer schema
* Validate data
* Convert into Parquet
* Persist optimized data

---

# 🧹 Data Cleaning

The following cleaning operations were performed:

* Null value analysis
* Duplicate transaction detection
* Data type validation
* Column formatting
* Outlier understanding

---

# 🔍 Exploratory Data Analysis (EDA)

The notebook performs detailed EDA using PySpark DataFrames and visualization libraries.

## Key Analysis Performed

### ✅ Fraud vs Non-Fraud Distribution

* Highly imbalanced dataset
* Fraud transactions represent only ~0.17%

### ✅ Transaction Amount Analysis

* Distribution of transaction values
* Fraud amount comparison
* Median & outlier analysis

### ✅ Time-Based Analysis

* Fraud occurrence by hour
* Peak fraud activity patterns
* Time trend exploration

### ✅ Correlation Analysis

* Feature correlation heatmap
* Top correlated variables
* Fraud-driving indicators

### ✅ Boxplot Analysis

* Comparison of important V-features
* Outlier detection

---

# 📈 Visualization Outputs

## 1️⃣ Fraud Class Distribution

![Fraud Distribution](outputs/plots/fraud_distribution.png)

---

## 2️⃣ Transaction Amount Distribution

![Transaction Amount](outputs/plots/transaction_amount_distribution.png)

---

## 3️⃣ Fraud Transactions by Time

![Time Analysis](outputs/plots/fraud_time_analysis.png)

---

## 4️⃣ Correlation Heatmap

![Correlation Heatmap](outputs/plots/correlation_heatmap.png)

---

## 5️⃣ Top Feature Boxplots

![Feature Boxplots](outputs/plots/feature_boxplots.png)

---

# ⚙️ Feature Engineering

Feature engineering steps include:

* Time-based feature extraction
* Scaling transaction amounts
* Feature selection
* Fraud behavior indicators

---

# 🗃️ Spark SQL Analysis

The project also uses Spark SQL for analytical querying.

### Sample SQL Queries

```sql
SELECT Class, COUNT(*)
FROM fraud_transactions
GROUP BY Class;
```

```sql
SELECT hour, COUNT(*) AS fraud_count
FROM fraud_transactions
WHERE Class = 1
GROUP BY hour
ORDER BY fraud_count DESC;
```

---

# ⚡ Performance Optimization

This project demonstrates PySpark optimization techniques.

## Optimization Techniques Used

* DataFrame caching
* Partition optimization
* Parquet storage format
* Reduced shuffle operations
* Efficient Spark transformations

---

# 💡 Business Insights

| Insight            | Finding                                       | Business Recommendation                  |
| ------------------ | --------------------------------------------- | ---------------------------------------- |
| Class imbalance    | Fraud transactions are extremely low          | Use balancing techniques in ML           |
| Fraud timing       | Fraud peaks during late-night hours           | Enable stronger nighttime authentication |
| Small-value frauds | Many frauds occur in smaller amounts          | Monitor micro-transactions               |
| Feature importance | Some V-features strongly correlate with fraud | Use them in fraud scoring models         |

---

# 📌 Key Learnings

* Hands-on PySpark DataFrame operations
* Large-scale data processing
* Spark SQL implementation
* Distributed analytics workflows
* Visualization integration with PySpark
* Performance tuning concepts

---

# ▶️ How to Run the Project

## Step 1: Clone Repository

```bash
git clone https://github.com/sahiamit1993/banking-fraud-pyspark.git
```

## Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

## Step 3: Start Jupyter Notebook

```bash
jupyter notebook
```

## Step 4: Run Notebook

Open:

```bash
banking_fraud_eda.ipynb
```

---

# 📦 Requirements

```text
pyspark
pandas
numpy
matplotlib
seaborn
plotly
jupyter
findspark
```

---

# 📷 Suggested GitHub Preview Images

You can save notebook charts inside:

```bash
outputs/plots/
```

Recommended screenshots:

* Fraud distribution chart
* Correlation heatmap
* Transaction amount histogram
* Time trend graph
* Boxplot analysis

These screenshots improve GitHub project presentation.

---

# 🎯 Future Improvements

* Fraud prediction model using Spark MLlib
* Real-time streaming fraud detection
* Kafka integration
* Airflow scheduling
* Docker deployment
* Cloud deployment on AWS EMR / Databricks

---

# 👨‍💻 Author

## Amit Kumar

Data Analyst | PySpark Enthusiast | Business Intelligence Developer

GitHub:

[https://github.com/sahiamit1993](https://github.com/sahiamit1993)

---

# ⭐ If You Like This Project

Give this repo
