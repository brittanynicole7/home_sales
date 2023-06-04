# Spark SQL/Spark Challenge

# Project Description 
- Create a Spark DataFrame for the dataset. 
- Create a temporary table of the DataFrame.
- Create a query that returns the average price, rounded to two decimal places, for a four-bedroom house that was sold in each year. 
- Create a query that returns the average prcie, rounded to two decimal places, for a home that has three bedrooms and three bathrooms. 
- Create a query that returns the average price of a home with three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet for each year built rounded to two decimal places. 
- Create a query that returns the view rating for the average price for homes that are greater than or equal to $350,000 rounded to two decimal places.
- Create a cache of the temporary "home_sales" table. 
- Run the query again with the cached temporary talb and compute the run time. 
- Create a partition of the home sales dataset by the "data_built" field and read the formatted parquet data. 
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

- Cached the temporary table home_sales. 

# Author 
-Brittany Wright github:brittanynicole7
