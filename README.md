# Amazon_Vine_Analysis

## Project Overview
Using one of the Amazon Vine program datasets we are going to perform an analysis to determine if there is any bias toward favorable reviews from Vine members.  To accomplish this task PySpark we will used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then PySpark, Pandas, or SQL will be used to determine if there is any bias.

For this assignment I picked the reviews on Video Games and will use PySpark for the analysis.

## Resources
* Source Data: [Amazon Vine Video Game Reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz)
* Software: Google Colab Notebook, PostgreSQL, pgAdmin 4, Amazon Web Service AWS, PySpark

# Analysis

## Deliverable 1 Perform ETL on Amazon Product Reviews
Using the cloud ETL process, the first step is creating an AWS RDS database with tables in pgAdmin for the Amazon Vine Video Game reviews dataset. The dataset will be transformed into four separate DataFrames that match the table schema in pgAdmin. Then the transformed data will be loaded into the appropriate tables and queries will be run in pgAdmin to confirm that the data has been uploaded.

Initial data Frame imported into Spark
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/PySpark%20File%20Import%20from%20S3%20bucket.PNG)

pgADmin Final Tables

customer_table
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/customers_table%20in%20pgAdmin.PNG)

products_table
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/product_table%20in%20pgAdmin.PNG)

review_id_table
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/review_id%20table%20in%20pgAdmin.PNG)

vine_table
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/vine_table%20in%20pgAdmin.PNG)

## Deliverable 2 Determine Bias of Vine Reviews

Determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid).

Paid Reviews Metrics
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/paid_reviews_metrics.PNG)

Unpaid Reviews Metrics
![](https://github.com/timbialek/Amazon_Vine_Analysis/blob/main/Resources/unpaid_reviews_metrics.PNG)



## Deliverable 3 Summary

Paid Reviews:

	* Total Paid Reviews: 94
	* Total Paid Reviews with 5 Stars: 48
	* % of Paid Reviews that were 5 Stars: 51.06%

Unpaid Reviews:

	* Total Unpaid Reviews: 40,471
	* Total Unpaid Reviews with 5 Stars: 15,663
	* % of Unpaid Reviews that were 5 Stars: 38.70%

In conclusion, for the Video Game dataset, it would seem that there is bias among the paid vine reviews for this particular data set since the percentage of 5 stars in the paid reviews is much higher than the percentage of 5 stars in the unpaid reviews.  

What we do not know is if this bias is present in all of the Amazon Vine datasets and a similar analysis would need to be performed for each to determine if there is bias in the overall program.
