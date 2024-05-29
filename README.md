# Home_Sales

In this challenge, you'll use your knowledge of SparkSQL to determine key metrics about home sales data. Then you'll use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

# Features:
Setup PySpark environment
Load and preprocess data
Perform data transformations
Execute SQL queries
Measure execution time of operations

# Requirements:
To run notebook the following must be installed to your environment (Mac):
Install Java - "brew install openjdk" 
Run the command "java -version" to verify Java version installed
Install PySpark - "pip install pyspark==3.5.1" (Could also use "pip install pyspark" to install most current version)
Run the command "spark-submit --version" to verify install was sucessful and version installed
Install Findspark - "conda install -c conda-forge findspark"
Install PyArrow - "conda install -c conda-forge pyarrow"
Run the command "conda list pyarrow" to verify installation success and version installed
Install Fastparquet - "conda install -c conda-forge fastparquet"
Run the command "conda list fastparquet" to verify install was successful and version installed

Libraries and dependancies:
# Import findspark and initialize
import findspark
# Import packages
findspark.init()
# Create a SparkSession
spark = SparkSession.builder.appName("SparkSQL").getOrCreate()
# Read in the AWS S3 bucket into a DataFrame.
from pyspark import SparkFiles

# Getting started:
Clone Home_Sales repository to local drive
Initialize Libraries and dependancies listed above in the Home_Sales.ipynb notebook
Execute the code to see results

# Instructions:
Rename the Home_Sales_starter_code.ipynb file as Home_Sales.ipynb.

Import the necessary PySpark SQL functions for this assignment.

Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.

Create a temporary table called home_sales.

Answer the following questions using SparkSQL:

What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

Cache your temporary table home_sales.

Check if your temporary table is cached.

Using the cached data, run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

Partition by the "date_built" field on the formatted parquet home sales data.

Create a temporary table for the parquet data.

Run the last query that calculates the average price of a home per "view" rating having an average home price greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

Uncache the home_sales temporary table.

Verify that the home_sales temporary table is uncached using PySpark.

# Table of contents:
parquet_home_sales - contains the output from the parquet component of the code
Home_Sales.ipynb - contains the code used to determine the outcomes to the questions above
README.md - contains the overview of the assignment, features of what was done in the assignment, requirements need to be installed to run notebook, instructions on the assignment, table of contents and references used to assist in the assignment.

# References:
Master documentation used to assist with structure of running pyspark and the different components involved:
https://spark.apache.org/docs/latest/api/python/index.html

Pypi documentation used to determine most current version of pyspark needed for the installation above:
https://pypi.org/project/pyspark/

Pyspark SQL cheat sheet used to verify correct calls to be used:
https://s3.amazonaws.com/assets.datacamp.com/blog_assets/PySpark_SQL_Cheat_Sheet_Python.pdf

ChatGPT used to assist in errors that came up during installation process and any other errors that came up during writing out the code:
[chatgpt.com](https://chatgpt.com/)

Class materials was referenced to assist with structure and find certain components of the code that was required.