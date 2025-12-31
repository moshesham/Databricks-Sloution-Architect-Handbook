## Hands-On PySpark with Open Source Datasets

This section provides a hands-on introduction to PySpark using Jupyter notebooks and open-source datasets. You'll learn how to perform common data manipulation, analysis, and machine learning tasks using PySpark DataFrames. This section assumes a basic understanding of Python and Spark.

### Environment Setup
Ensure you have the following installed:

- Python (3.x recommended)
- Jupyter Notebook
- Apache Spark with PySpark 
- FindSpark ( to help locate spark in your system for jupyter notebooks)
  
You can install these using `pip`:
```bash
pip install jupyter findspark pyspark
```
If you are new to Spark please feel free to read this comprehensive guide: https://spark.apache.org/docs/latest/api/python/getting_started/index.html

### Notebook Tutorials

These notebooks provide a practical introduction to PySpark concepts and operations.

#### 1. PySpark DataFrame Basics

**Objective:** Learn the basics of creating and manipulating PySpark DataFrames.

**Topics Covered:**

*   Creating DataFrames from lists, RDDs, and external data sources.
*   Basic DataFrame operations:
    *   `printSchema()`
    *   `show()`
    *   `select()`
    *   `filter()`
    *   `withColumn()`
    *   `withColumnRenamed()`
*   Handling null values.

**Dataset:**  A simple synthetic dataset created using Python lists, and the [California Housing Prices](https://www.kaggle.com/datasets/camnugent/california-housing-prices) dataset from Kaggle. 

**Notebook:** [01_DataFrame_Basics.ipynb](notebooks/01_DataFrame_Basics.ipynb) 

#### 2. DataFrame Operations and Transformations

**Objective:** Explore more advanced DataFrame operations and transformations.

**Topics Covered:**

*   Joining DataFrames.
*   Aggregations and `groupBy()`.
*   Sorting.
*   Window functions.
*   Explode array and map columns to rows.
*   UDFs (User-Defined Functions).
*   Handling complex data types (arrays, maps).

**Dataset:** [Movies Dataset](https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset) from Kaggle.

**Notebook:** [02_DataFrame_Operations.ipynb](notebooks/02_DataFrame_Operations.ipynb)

#### 3. Working with External Data Sources

**Objective:** Learn how to read and write data from various external sources.

**Topics Covered:**

*   Reading and writing CSV files.
*   Reading and writing Parquet files.
*   Reading and writing JSON files.
*   Reading from a relational database (e.g., MySQL, PostgreSQL) using JDBC. (Optional)

**Dataset:**
*   CSV: [New York City Airbnb Open Data](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data)
*   Parquet: [Parquet Datasets from the Apache project](https://github.com/apache/spark/tree/master/data/parquet)
*   JSON: [Sample JSON Data](https://github.com/dariusk/corpora/blob/master/data/humans/occupations.json) from the corpora collection of public domain data. 

**Notebook:** [03_External_Data_Sources.ipynb](notebooks/03_External_Data_Sources.ipynb)

#### 4. PySpark SQL

**Objective:** Learn how to use SQL queries with PySpark.

**Topics Covered:**

*   Creating temporary tables/views.
*   Running SQL queries using `spark.sql()`.
*   Using `GROUP BY`, `HAVING`, `ORDER BY`.
*   Window functions in SQL.
*   Advanced SQL concepts (CTEs, analytical functions).

**Dataset:** [World Happiness Report](https://www.kaggle.com/datasets/unsdsn/world-happiness) from Kaggle.

**Notebook:** [04_PySpark_SQL.ipynb](notebooks/04_PySpark_SQL.ipynb)

#### 5. Introduction to PySpark MLlib

**Objective:** Get a basic introduction to machine learning with PySpark MLlib.

**Topics Covered:**

*   Data preprocessing for machine learning.
*   Feature engineering (VectorAssembler, StringIndexer, OneHotEncoder).
*   Training a simple linear regression model.
*   Model evaluation.

**Dataset:** [Diabetes dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) from the UCI Machine Learning Repository.

**Notebook:** [05_Introduction_to_MLlib.ipynb](notebooks/05_Introduction_to_MLlib.ipynb)

### Project Ideas

These project ideas allow you to apply your PySpark skills to real-world datasets and build end-to-end data processing pipelines.

#### Project 1: E-commerce Product Analysis

**Dataset:** [Amazon Product Data](https://www.kaggle.com/datasets/PromptCloudHQ/amazon-reviews-unlocked-mobile-phones) or [Flipkart Products Dataset](https://www.kaggle.com/datasets/dhruvildave/flipkart-products) from Kaggle

**Tasks:**

1. **Data Loading and Cleaning:**
    *   Load the dataset into a PySpark DataFrame.
    *   Handle missing values, duplicates, and inconsistencies.
    *   Convert data types if necessary.
2. **Exploratory Data Analysis (EDA):**
    *   Analyze product categories, ratings, and reviews.
    *   Identify top-selling products and brands.
    *   Explore the relationship between price, ratings, and reviews.
    *   Visualize findings using charts and graphs (you can use matplotlib or seaborn within PySpark).
3. **Sentiment Analysis:**
    *   Perform sentiment analysis on product reviews using PySpark MLlib's NLP capabilities (or a library like TextBlob, if applicable within your Spark setup).
    *   Classify reviews as positive, negative, or neutral.
4. **Recommendation System (Optional):**
    *   Build a simple product recommendation system using collaborative filtering techniques (e.g., ALS in MLlib).

#### Project 2:  Analyzing Flight Delays

**Dataset:** [Flight Delay and Cancellation Data](https://www.kaggle.com/datasets/yuanyuwendymu/airline-delay-and-cancellation-data-2009-2018) from Kaggle.

**Tasks:**

1. **Data Ingestion and Preprocessing:**
    *   Load the flight data into a PySpark DataFrame.
    *   Handle missing data and outliers.
    *   Extract relevant features (e.g., date, time, origin, destination, airline, delay).
2. **Data Exploration:**
    *   Analyze flight delays by airline, origin, destination, and time of day/year.
    *   Identify the major causes of delays.
    *   Visualize delay patterns using appropriate charts.
3. **Predictive Modeling:**
    *   Build a machine learning model to predict flight delays using PySpark MLlib (e.g., linear regression, decision trees).
    *   Evaluate the model's performance using appropriate metrics (e.g., RMSE, MAE).
4. **Feature Engineering:**
    * Create new features that might improve prediction such as rolling average of delays for an airport.

#### Project 3: Website Traffic Analysis

**Dataset:**  [Web Server Log Data](https://github.com/elastic/examples/tree/master/Common%20Data%20Formats/apache_logs) (Example Apache logs from Elastic) or any website traffic dataset.

**Tasks:**

1. **Data Loading and Parsing:**
    *   Load the web server logs into a PySpark DataFrame.
    *   Parse the log lines to extract relevant fields (e.g., IP address, timestamp, request URL, status code, user agent). You might need to use regular expressions for parsing.
2. **Data Analysis:**
    *   Analyze website traffic patterns by time of day, day of the week, and geographic location (if available).
    *   Identify the most popular pages and referral sources.
    *   Calculate bounce rates and session durations.
    *   Detect any unusual traffic patterns or anomalies (e.g., potential security threats).
3. **Data Aggregation and Reporting:**
    *   Create aggregated reports on website traffic, user behavior, and performance metrics.
    *   Visualize the findings using charts and dashboards.

### Getting Started with the Notebooks

1. **Clone the Repository:**

```bash
git clone https://github.com/your-username/databricks-solution-architect-handbook.git
cd databricks-solution-architect-handbook
```

2. **Navigate to the `notebooks` directory:**

```bash
cd notebooks
```

3. **Start Jupyter Notebook:**

```bash
jupyter notebook
```
4. **Open and run the notebooks in order.**

### Tips for Success

*   **Read the documentation:** Familiarize yourself with the PySpark documentation: [https://spark.apache.org/docs/latest/api/python/index.html](https://spark.apache.org/docs/latest/api/python/index.html)
*   **Experiment:** Don't be afraid to experiment with the code and try different things.
*   **Ask for help:** If you get stuck, ask for help on the [Databricks Community Forums](https://community.databricks.com/), [Stack Overflow](https://stackoverflow.com/questions/tagged/pyspark), or other online resources.
*   **Practice regularly:** The more you practice, the better you'll become at using PySpark.
*   **Break down complex tasks:** Divide large tasks into smaller, more manageable steps.
*   **Use comments:** Add comments to your code to explain what it does.
*   **Test your code:** Thoroughly test your code to make sure it works as expected.
* **Version Control** Use git to manage changes in your code
* **Optimize:** Always look for ways to make your Spark code run more efficiently

### Enjoy your journey to becoming a PySpark expert!
