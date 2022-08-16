# big-data-challenge
ETL process using RDS database

## ETL

## Source

Many of Amazon's shoppers depend on product reviews to make a purchase. Amazon makes these datasets publicly available. They are quite large and can exceed the capacity of local machines. One dataset alone contains over 1.5 million rows; with over 40 datasets, data analysis can be very demanding on the average local computer. 

The goal for this assignment was to perform the ETL process completely in the cloud and upload a DataFrame to an RDS instance.

## Extract

From Amazon [reviews dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt) I chose:

* Cameras DB: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Camera_v1_00.tsv.gz
  
  Which has 1.801.974 rows.

* Video Games DB: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz
  
  Which has 1.785.997 rows.

![Bucket](/AWS-Screenshots/aws-bucket.JPG)

The two ETL processes were performed separately: in the [big_data_model](/big_data_model.ipynb) is the ETL for the Camera DB, and in [big_data_model_2](/big_data_model_2.ipynb) is the ETL for the Video Game DB.

![DB](/AWS-Screenshots/aws-db1.JPG)

## Transform 

I have transformed the dataset to fit the tables in my RDS database. You can check the [schema file here](/schema.sql). 

## Load

I have loaded the DataFrames that correspond to tables into an RDS instance.

![Postgres](/AWS-Screenshots/postgres-cameras-query.JPG)
![Postgres](/AWS-Screenshots/postgres-vgames-query.JPG)

- - -

## References

Amazon customer Reviews Dataset. (n.d.). Retrieved April 08, 2021, from: [https://s3.amazonaws.com/amazon-reviews-pds/readme.html](https://s3.amazonaws.com/amazon-reviews-pds/readme.html)

- - -

© 2022 University of Birmingham / Data Analysis Assignment by DianaAF	
