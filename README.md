# Spark SQL/Spark Challenge

## Note: 
See the Home_Sales.ipynb file for the code for the assignment. I did not use the colab file for this assignment.

# Project Description 
- Create a Spark DataFrame for the dataset. 
- Create a temporary table of the DataFrame.
- Create a query that returns the average price, rounded to two decimal places, for a four-bedroom house that was sold in each year. 
- Create a query that returns the average price, rounded to two decimal places, for a home that has three bedrooms and three bathrooms. 
- Create a query that returns the average price of a home with three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet for each year built rounded to two decimal places. 
- Create a query that returns the view rating for the average price for homes that are greater than or equal to $350,000 rounded to two decimal places.
- Create a cache of the temporary "home_sales" table. 
- Run the query again with the cached temporary table and compute the run time. 
- Create a partition of the home sales dataset by the "date_built" field and read the formatted parquet data. 
- Create a temporary table of the parquet data. 
- Run the query again and compute the run time. 
- Uncache the "home_sales" temporary table. 

# Software and Files
- import findspark
- from pyspark.sql import SparkSession
- from pyspark import SparkFiles
- url: https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv

# Output/Analyses

- Imported findspark and and initialized it. 
<img width="958" alt="Screenshot 2023-06-04 at 10 52 03 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/5fdc8644-ea3d-42e4-8e97-974dca20e269">

- Imported packages and created a SparkSession. 
<img width="937" alt="Screenshot 2023-06-04 at 10 54 39 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/f50cb226-1a0f-44ba-9cf7-f6c4dd2f02f2">

- Read in the AWS S3 bucket into a DataFrame.
<img width="1168" alt="Screenshot 2023-06-04 at 10 55 18 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/8b8b123d-04c5-4149-ba9a-79125d50c28c">

- Created a temporary view of the DataFrame. 
<img width="748" alt="Screenshot 2023-06-04 at 10 55 44 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/0fea049b-4a9e-4ddd-a8c1-55d49cb6c6bf">

- Created a query to find the average price of a four bedroom house sold in each year rounded to two decimal places. 
<img width="1168" alt="Screenshot 2023-06-04 at 10 56 25 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/d4272fa6-016e-4320-8057-5b2a4a4b88b4">

- Created a query to find the average price of a home for each year the home was built that has 3 bedrooms and 3 bathrooms rounded to the nearest two decimal places. 
<img width="1171" alt="Screenshot 2023-06-04 at 10 57 24 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/b757a5cb-c856-4b64-9d18-ffc7c4f3a2f8">

- Created a query to find the average price of a home for each year built with 3 bedrooms, 3 bathrooms, two floors, and greater than or equal to 2,000 square feet rounded to two decimal places. 
<img width="1169" alt="Screenshot 2023-06-04 at 10 58 19 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/b18c6b6f-7c53-43e4-a653-950f29ef7d30">

- Created a query to find the "view" rating for the average price of a home, rounded to two decimal places, where homes are greater than or equal to $350,000 and determined the run time. 
<img width="1171" alt="Screenshot 2023-06-04 at 10 59 29 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/f60796d6-7ac0-4a8f-86e5-6859ea179fd7">
<img width="656" alt="Screenshot 2023-06-04 at 10 59 40 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/c9af5e79-b5f8-45b5-8eed-7337b90ab868">

- Cached the temporary table home_sales and checked to make sure the table was cached.
<img width="756" alt="Screenshot 2023-06-04 at 11 08 26 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/49f5f93a-a413-4bdf-b76f-0dd517a95c65">
<img width="1095" alt="Screenshot 2023-06-04 at 11 08 51 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/9e7ae6b0-8d6f-44f9-80b1-6606ff2fae82">

- Ran the query that filters out the view ratings with an average price greater than or equal to $350,000 and determined the runtime using the cached table. 
<img width="1159" alt="Screenshot 2023-06-04 at 11 10 15 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/d7fffca8-edc9-4fb8-99db-76dcc7e8a1e0">
<img width="747" alt="Screenshot 2023-06-04 at 11 10 29 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/a76f3996-1ad0-4a2b-b45c-8dc845fa0d52">

- Partitioned the data by "date_built" on the formatted parquet home sales data. 
<img width="1155" alt="Screenshot 2023-06-04 at 11 11 10 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/e9282780-1b05-4a22-8946-648528f23a32">

- Read the formatted parquet data. 
<img width="954" alt="Screenshot 2023-06-04 at 11 11 33 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/862edcc5-2cf1-4902-9950-0efb74d4539b">

- Created a temporary table for the parquet data. 
<img width="877" alt="Screenshot 2023-06-04 at 11 11 58 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/040eef68-8e5a-4a16-9bb5-00a7631a2fe7">

- Ran the query that filters out the view ratings with average price greater than or equal to $350,000 with the parquet DataFrame and determined the runtime and compared it to the cached version. 
<img width="919" alt="Screenshot 2023-06-04 at 11 13 06 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/6db76e68-3429-4b63-ae7e-f1943ce3772c">
<img width="740" alt="Screenshot 2023-06-04 at 11 13 20 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/9f5d6619-1bd9-4006-b3b1-8a019710306a">

- Uncached the home_sales temporary table.
<img width="958" alt="Screenshot 2023-06-04 at 11 13 42 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/0ee2adfa-b51d-42aa-bd16-a5d8fc1813dc">

- Checked to make sure the home_sales data is no longer cached. 
<img width="938" alt="Screenshot 2023-06-04 at 11 14 05 AM" src="https://github.com/brittanynicole7/home_sales/assets/119909433/0a061647-a81b-4f4e-a733-78d543add5e9">

# Author 
-Brittany Wright github:brittanynicole7
