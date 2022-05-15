# Amazon_Vine_Analysis

## Project oOverview
Using one of the Amazon Vine program datasets we are going to perform an analysis to determine if there is any bias toward favorable reviews from Vine members.  To accomplish this task PySpark we will used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then PySpark, Pandas, or SQL will be used to determine if there is any bias.
For this assignment I picked the reviews for Video games and the use of PySpark for the analysis.

## Resources
* Source Data: ![Amazon Vine Video Game Reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz)
* Software : Google Colab Notebook, PostgreSQL, pgAdmin 4, Amazon Web Service AWS, PySpark

# Analysis

## Deliverable 1 Perform ETL on Amazon Product Reviews
Using the cloud ETL process, we are creating an AWS RDS database with tables in pgAdmin using the Amazon Vine Video Game reviews dataset. The dataset will be transformed into four separate DataFrames that match the table schema in pgAdmin. Then the transformed data will be loaded into the appropriate tables and queries will be run in pgAdmin to confirm that the data has been uploaded.

Initial datafrrame imported into Spark
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/PySpark%20File%20Import%20from%20S3%20bucket.PNG)

pgADmin Final Tables

customer_table
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/customers_table%20in%20pgAdmin.PNG)

products_table
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/product_table%20in%20pgAdmin.PNG)

review_id_table
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/review_id%20table%20in%20pgAdmin.PNG)

vine_table
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/customers_table%20in%20pgAdmin.PNG)

## Deliverable 2


## Deliverable 3


t-test for lot 1:
![](https://gihub.com/timbialek/MechaCar_Statistical_Analysis/blob/main/Resources/t-test_lot_1.png)
