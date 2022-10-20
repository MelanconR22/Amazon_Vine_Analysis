# Amazon_Vine_Analysis

## Overview of the analysis: Explain the purpose of this analysis.

For this project, i have been tasked with analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, I had access to approximately 50 datasets. Each one contained reviews of a specific product, from clothing apparel to wireless products. I selected a dataset from the sports product category and used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. I then used PySpark, Pandas, or SQL to determine if there was any bias toward favorable reviews from Vine members in your dataset.

## Results: Using bulleted lists and images of DataFrames as support, address the following questions:

To help with the following analysis, a rating total dataframe was created that would determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid).  The following dataframe image contains this information:

![reviews](https://user-images.githubusercontent.com/107599510/197059791-4bd716ca-0ba1-4cbf-b082-a4a22e2fbcb6.png)

#### How many Vine reviews and non-Vine reviews were there?

For this product category, there were a total of 334 vine reviews and 61,614 non-vine reviews.  The total number of reviews for this product equaled 61,948 which breaksdown to 0.54% vine reviews and 99.46% non-vine reviews.  

#### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

In total, there were 32,804 5 star reviews for the products.   From an overall standpoint, that means that 52.95% of total reviews recieved were 5 star reviews. Of the total number of 5 star reviews, 139 were vine reviews while 32,665 were non-vine reviews. 

#### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?


## Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
