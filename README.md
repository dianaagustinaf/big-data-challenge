# big-data-challenge
ETL process using RDS database


## Background

Many of Amazon's shoppers depend on product reviews to make a purchase. Amazon makes these datasets publicly available. They are quite large and can exceed the capacity of local machines. One dataset alone contains over 1.5 million rows; with over 40 datasets, data analysis can be very demanding on the average local computer. 

The first goal for this assignment was to perform the ETL process completely in the cloud and upload a DataFrame to an RDS instance. The second goal was to use PySpark or SQL to perform a statistical analysis of selected data.

1. Create DataFrames to match production-ready tables from two big Amazon customer review datasets.

2. Analyze whether reviews from Amazon's Vine program are trustworthy.

- - -

## Instructions

* Use the provided schema to create tables in your RDS database.

* Create two separate Google Colab notebooks and **extract** any two datasets from the list at [review dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt). Put each dataset into its own notebook.

  **Note:** You could ETL both data sources in a single Colab notebook, but it will be easier to work with these large S3 data sources in separate notebooks.

* Be sure to handle the header correctly. If you read the file without the header parameter, you may find that the column headers are included in the table rows.

* Complete the following steps for each notebook (one dataset per notebook).

  * Count the number of records (rows) in the dataset.

  * Transform the dataset to fit the tables in the [schema file](../Resources/schema.sql). Be sure that the DataFrames match in data type and in column name.

  * Load the DataFrames that correspond to tables into an RDS instance. **Note:** This process can take up to 10 minutes for each. Ensure that everything is correct before uploading.

- - -

## References

Amazon customer Reviews Dataset. (n.d.). Retrieved April 08, 2021, from: [https://s3.amazonaws.com/amazon-reviews-pds/readme.html](https://s3.amazonaws.com/amazon-reviews-pds/readme.html)

- - -

© 2022 University of Birmingham / Data Analysis Assignment by DianaAF	
