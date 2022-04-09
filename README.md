# Amazon Vine Analysis

### Overview
In this project, we’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. We will pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Afterwhich, we'll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. In this project, we will be focusing on Amazon reviews of watches.

### Resources
#### Dataset: Amazon Watches Reviews
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Watches_v1_00.tsv.gz

### Results
#### Deliverable 1: Perform ETL on Amazon Watches Reviews
* Amazon Review of dataset is extracted as a DataFrame:

    [Resources/Amazon_Reviews_ETL.ipynb.pdf](Amazon_Reviews_ETL.ipynb.pdf)

* Extracted dataset is transformed into 4 DataFrames with correct columns:

    [Resources/Amazon_Reviews_ETL.ipynb.pdf](Amazon_Reviews_ETL.ipynb.pdf)

* 4 DataFrames are loaded into pgAdmin:

![Customer_Table](Resources/customers_table.png "Customer Table")

![Products_Table](Resources/products_table.png "Products Table")

![Review_ID_Table](Resources/review_id_table.png "Review Table")

![Vine_Table](Resources/vine_table.png "Vine Table")

#### Deliverable 2: Determine Bias of Vine Reviews
* PySpark method was used:

    [Vine_Review_Analysis.ipynb](Vine_Review_Analysis.ipynb)

* Data is filtered to create a DataFrame where there are 20+ total votes:

    [Vine_Review_Analysis.ipynb](Vine_Review_Analysis.ipynb)    

* Data is filtered to create a DataFrame where percentage of helpful_votes is >= 50%:
    
    [Vine_Review_Analysis.ipynb](Vine_Review_Analysis.ipynb)
    
* Data is filtered where there is a Vine review:

    [Vine_Review_Analysis.ipynb](Vine_Review_Analysis.ipynb)
    
* Data is filtered where there is no Vine review:

    [Vine_Review_Analysis.ipynb](Vine_Review_Analysis.ipynb)

* The total number of reviews, the number of 5-star reviews, and the percentage 5-star reviews are calculated for all Vine and non-Vine reviews:

### Summary
