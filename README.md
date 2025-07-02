# Walmart_sales_project
## Project Overview
This project is an end-to-end data analysis solution designed to extract critical business insights from Walmart sales data. We utilize Python for data processing and analysis, SQL for advanced querying, and structured problem-solving techniques to solve key business questions. The project is ideal for data analysts looking to develop skills in data manipulation, SQL querying, and data pipeline creation.

## Project Steps

### 1. Set Up the Environment
   - **Tools Used**: Visual Studio Code (VS Code), Python, SQL (MySQL)
   - **Goal**: Create a structured workspace within VS Code and organize project folders for smooth development and data handling.

### 2. Set Up Kaggle API
   - **API Setup**: Obtain your Kaggle API token from [Kaggle](https://www.kaggle.com/) by navigating to your profile settings and downloading the JSON file.
   - **Configure Kaggle**: 
      - Place the downloaded `kaggle.json` file in your local `.kaggle` folder.
      - Use the command `kaggle datasets download -d <dataset-path>` to pull datasets directly into your project.

### 3. Download Walmart Sales Data
   - **Data Source**: Use the Kaggle API to download the Walmart sales datasets from Kaggle.
   - **Dataset Link**: [Walmart Sales Dataset](https://github.com/avii2583/Walmart_sales_project/blob/main/Walmart.csv)
   - **Storage**: Save the data in the `data/` folder for easy reference and access.

### 4. Install Required Libraries and Load Data
   - **Libraries**: Install necessary Python libraries using:
     ```bash
     pip install pandas numpy sqlalchemy mysql-connector-python psycopg2
     ```
   - **Loading Data**: Read the data into a Pandas DataFrame for initial analysis and transformations.

### 5. Explore the Data
   - **Goal**: Conduct an initial data exploration to understand data distribution, check column names, types, and identify potential issues.
   - **Analysis**: Use functions like `.info()`, `.describe()`, and `.head()` to get a quick overview of the data structure and statistics.

### 6. Data Cleaning
   - **Remove Duplicates**: Identify and remove duplicate entries to avoid skewed results.
   - **Handle Missing Values**: Drop rows or columns with missing values if they are insignificant; fill values where essential.
   - **Fix Data Types**: Ensure all columns have consistent data types (e.g., dates as `datetime`, prices as `float`).
   - **Currency Formatting**: Use `.replace()` to handle and format currency values for analysis.
   - **Validation**: Check for any remaining inconsistencies and verify the cleaned data.

### 7. Feature Engineering
   - **Create New Columns**: Calculate the `Total Amount` for each transaction by multiplying `unit_price` by `quantity` and adding this as a new column.
   - **Enhance Dataset**: Adding this calculated field will streamline further SQL analysis and aggregation tasks.

### 8. Load Data into MySQL
   - **Set Up Connections**: Connect to MySQL using `sqlalchemy` and load the cleaned data into each database.
   - **Table Creation**: Set up tables in both MySQL using Python SQLAlchemy to automate table creation and data insertion.
   - **Verification**: Run initial SQL queries to confirm that the data has been loaded accurately.

### 9. SQL Analysis: Complex Queries and Business Problem Solving
   - **Business Problem-Solving**: Write and execute complex SQL queries to answer critical business questions, such as:
     - Revenue trends across branches and categories.
     - Identifying best-selling product categories.
     - Sales performance by time, city, and payment method.
     - Analyzing peak sales periods and customer buying patterns.
     - Profit margin analysis by branch and category.
  


## Data Visualization & Insights

This section highlights key visual analyses performed to uncover trends, patterns, and business opportunities within the Walmart sales dataset. Each visual explores a specific question aimed at improving business decisions.

---

### 1. Analyze Sales Distribution by Category
- **Question**: What is the distribution of total sales across product categories?
- **Objective**: Identify high-performing categories and detect underperformers to guide inventory and promotion strategies.

---

### 2. Evaluate Category-Level Customer Satisfaction
- **Question**: What is the average customer rating for each product category?
- **Objective**: Understand customer sentiment across different product types to inform quality control and product development.

---

### 3. Assess Ratings Across Spending Tiers
- **Question**: What is the average customer rating across different transaction amount ranges?
- **Objective**: Analyze whether customer satisfaction changes with transaction value, helping to inform pricing and loyalty strategies.

---

### 4. Compare Transaction Value by Shift and Payment Method
- **Question**: What is the average transaction value by shift and payment method?
- **Objective**: Uncover patterns in purchasing behavior by time of day and payment preference to optimize staffing and payment systems.

---

### 5. Examine Overall Rating Distribution
- **Question**: What is the distribution of customer ratings across all transactions?
- **Objective**: Provide a high-level view of customer satisfaction and detect skewness or gaps that may indicate operational issues.

---

### 6. Correlate Spending with Rating Levels
- **Question**: How does average transaction amount vary across different customer rating levels?
- **Objective**: Discover whether spending behavior correlates with satisfaction, offering insight into high-value customer experience.

---

