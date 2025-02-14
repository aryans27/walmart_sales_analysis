# Walmart Data Analysis: SQL + Python Project

## Project Overview

![Project Pipeline](https://github.com/aryans27/walmart_sales_analysis/blob/main/walmart_project-piplelines.png)


This project provides a comprehensive data analysis solution aimed at deriving valuable business insights from Walmart sales data. We leverage Python for data processing and analysis, SQL for complex querying, and structured problem-solving methods to address key business questions. It's an excellent opportunity for data analysts to enhance their skills in data manipulation, SQL queries, and building data pipelines.

---

## Project Steps

### 1. Set Up the Environment
   - **Tools Used**: Visual Studio Code (VS Code), Python, SQL
   - **Goal**: Create a structured workspace within VS Code and organize project folders for smooth development and data handling.

### 2. Set Up Kaggle API
   - **API Setup**: Obtain your Kaggle API token from [Kaggle](https://www.kaggle.com/) by navigating to your profile settings and downloading the JSON file.
   - **Configure Kaggle**: 
      - Place the downloaded `kaggle.json` file in your local `.kaggle` folder.
      - Use the command `kaggle datasets download -d <dataset-path>` to pull datasets directly into your project.

### 3. Download Walmart Sales Data
   - **Data Source**: Use the Kaggle API to download the Walmart sales datasets from Kaggle.
   - **Dataset Link**: [Walmart Sales Dataset](https://www.kaggle.com/najir0123/walmart-10k-sales-datasets)
   - **Storage**: Save the data in the `data/` folder for easy reference and access.

### 4. Install Required Libraries and Load Data
   - **Libraries**: Install necessary Python libraries using:
     ```bash
     pip install pandas numpy sqlalchemy
     ```
   - **Loading Data**: Read the data into a Pandas DataFrame for initial analysis and transformations.

### 5. Explore the Data
   - **Goal**: Perform an initial data exploration to analyze the distribution of the data, examine column names and data types, and identify any potential issues.
   - **Analysis**: Use functions like `.info()`, `.describe()`, and `.head()` to get a quick overview of the data structure and statistics.

### 6. Data Cleaning
   - **Eliminate Duplicates**: Detect and remove duplicate records to prevent distorted outcomes.
   - **Address Missing Values**: Remove rows or columns with missing data if they are not important; fill in missing values where necessary.
   - **Correct Data Types**: Ensure that all columns have the appropriate data types (e.g., dates as `datetime`, prices as `float`).
   - **Format Currency**: Use `.replace()` to clean and standardize currency values for analysis.
   - **Data Validation**: Review the dataset for any remaining discrepancies and confirm the data is properly cleaned.

### 7. Feature Engineering  
   - **Generate New Columns**: Create a `Total Amount` column for each transaction by multiplying `unit_price` by `quantity`. Add this new column to the dataset.  
   - **Improve Dataset**: Adding this calculated field will facilitate smoother SQL analysis and aggregation tasks.

### 8. Load Data into MySQL and PostgreSQL  
   - **Establish Connections**: Use `sqlalchemy` to connect to MySQL and PostgreSQL, and load the cleaned data into both databases.  
   - **Table Creation**: Automate the creation of tables and data insertion in MySQL and PostgreSQL using Python's SQLAlchemy.  
   - **Validation**: Run sample SQL queries to verify that the data has been loaded correctly.

### 9. SQL Analysis: Advanced Queries and Business Problem Solving  
   - **Address Business Questions**: Write and execute complex SQL queries to solve key business problems, such as:  
     - Analyzing revenue trends across branches and categories.  
     - Identifying top-selling product categories.  
     - Evaluating sales performance by time, location, and payment method.  
     - Analyzing peak sales periods and customer purchasing behaviors.  
     - Assessing profit margins by branch and category.  
   - **Record Findings**: Keep detailed notes on the objective, methodology, and outcomes of each query.

### 10. Project Publishing and Documentation  
   - **Comprehensive Documentation**: Create structured documentation of the entire process, either in Markdown or a Jupyter Notebook.  
   - **Project Deployment**: Publish the final project on GitHub or a similar version control platform, including:  
     - The `README.md` file (overview document).  
     - Jupyter Notebooks (if used).  
     - SQL query scripts.  
     - Data files (if accessible) or instructions on how to obtain them.
---

## Requirements

- **Python 3.8+**
- **SQL Databases**: MySQL
- **Python Libraries**:
  - `pandas`, `numpy`, `sqlalchemy`, `mysql-connector-python`
- **Kaggle API Key** (for data downloading)

## Getting Started

1. Clone the repository:
   ```bash
   git clone <repo-url>
   ```
2. Install Python libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up your Kaggle API, download the data, and follow the steps to load and analyze.

---

## Project Structure

```plaintext
|-- data/                     # Raw data and transformed data
|-- sql_queries/              # SQL scripts for analysis and queries
|-- notebooks/                # Jupyter notebooks for Python analysis
|-- README.md                 # Project documentation
|-- requirements.txt          # List of required Python libraries
|-- main.py                   # Main script for loading, cleaning, and processing data
```
---

## Results and Insights

This section will include your analysis findings:
- **Sales Insights**: Key categories, branches with highest sales, and preferred payment methods.
- **Profitability**: Insights into the most profitable product categories and locations.
- **Customer Behavior**: Trends in ratings, payment preferences, and peak shopping hours.

## Future Enhancements

Possible extensions to this project:
- Integration with a dashboard tool (e.g., Power BI or Tableau) for interactive visualization.
- Additional data sources to enhance analysis depth.
- Automation of the data pipeline for real-time data ingestion and analysis.

---

## License

This project is licensed under the MIT License. 

---

## Acknowledgments

- **Data Source**: Kaggle’s Walmart Sales Dataset
- **Inspiration**: Walmart’s business case studies on sales and supply chain optimization.

---
