# 📈 Retail Data ETL & Analytics Pipeline

![Python](https://img.shields.io/badge/Python-3.9-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data_Processing-150458?style=for-the-badge&logo=pandas&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-Data_Warehouse-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Analysis-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

## 📖 Overview
This project implements an end-to-end **Data Engineering Pipeline** that processes historical US Retail Trade data (1992–2021). The goal is to transform raw, unstructured Excel/CSV extracts into a clean, normalized SQL database to enable trend analysis and visualization of long-term economic patterns.

The solution demonstrates a robust **ETL (Extract, Transform, Load)** workflow, handling data cleaning, schema normalization, and insertion into a relational warehouse, followed by analytical queries to track industry-specific growth (e.g., E-commerce vs. Traditional Retail).

## 🏗️ Architecture

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/4b0c25f6-1f8c-4e6f-8058-2358d3ddbc3c" />


## 🚀 Key Features
* **Automated Bulk Ingestion:** The `ETL1.ipynb` notebook iteratively processes decades of monthly data files (flat structure), handling inconsistent formatting and missing values.
* **Data Transformation:** Cleansing logic to standardize column names, handle suppressed values (e.g., `(S)`), and convert data types for accurate calculation.
* **SQL Integration:** Uses `mysql.connector` and `SQLAlchemy` to load processed data into a structured relational schema (`module8` database).
* **Trend Analysis:** `PythonQueries.ipynb` executes complex SQL queries to visualize seasonality and sector performance (e.g., comparing "Men's Clothing" vs. "Women's Clothing" sales over 30 years).

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Libraries:** Pandas, NumPy, MySQL Connector, SQLAlchemy, Matplotlib, Seaborn
* **Database:** MySQL
* **Tools:** Jupyter Notebook

## 📂 Project Structure
All files are located in the root directory for ease of execution.

```text
├── ETL1.ipynb              # Main ETL pipeline: Reads CSVs -> Cleans -> Loads to MySQL
├── PythonQueries.ipynb     # Analytics: Queries MySQL -> Generates Visualizations
├── MRTS1.xlsx - 1992.csv   # Raw historical data (Yearly files from 1992-2021)
├── ...                     # (Additional data files)
├── MRTS1prueba.xlsx - *.csv # Validation datasets
└── README.md               # Project documentation
````

## 💻 Getting Started

### 1\. Prerequisites

  * **Python 3.x** and Jupyter Lab/Notebook.
  * **MySQL Server** running locally.
  * Python libraries:
    ```bash
    pip install pandas numpy mysql-connector-python sqlalchemy matplotlib seaborn openpyxl
    ```

### 2\. Database Setup

Ensure you have a MySQL instance running. The ETL script is configured to connect to `localhost`.

  * **Database Name:** `module8` (Created automatically by the script if configured).
  * **Credentials:** Update the `mysql.connector.connect` parameters in the notebooks to match your local user/password.

### 3\. Running the Pipeline

1.  **Run ETL Process:**
    Open `ETL1.ipynb` and execute all cells. This will:

      * Read the raw CSV files from the current folder.
      * Clean and restructure the data.
      * Load the data into the MySQL table.

2.  **Run Analysis:**
    Open `PythonQueries.ipynb` to execute SQL queries against the database and generate charts showing retail trends.

## 📊 Sample Insights

*(From PythonQueries.ipynb)*

  * **Seasonality:** Clear cyclical peaks in December across most retail sectors.
  * **Pandemic Impact:** Visible disruption in trend lines during 2020, with rapid recovery in specific sub-sectors.
  * **Digital Shift:** Long-term uptrend in "Electronic Shopping" compared to brick-and-mortar counterparts.

## 👤 Author

**José Antonio Morfín Guerrero**

  * Digital Transformation Leader | Data Engineer
  * [LinkedIn](https://www.google.com/search?q=https://linkedin.com/in/joseantoniomorfinguerrero)
  * [Portfolio](https://joseantoniomorfin.name)

<!-- end list -->

```
```
