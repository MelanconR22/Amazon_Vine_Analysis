# Amazon_Vine_Analysis

## Overview of the analysis: 

For this project, i have been tasked with analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, I had access to approximately 50 datasets. Each one contained reviews of a specific product, from clothing apparel to wireless products. I selected a dataset from the sports product category and used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. I then used PySpark, Google Colab, Pandas and SQL to determine if there was any bias toward favorable reviews from Vine members in your dataset.

## Results: Using bulleted lists and images of DataFrames as support, address the following questions:

To help with the following analysis, a rating total dataframe was created that would determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid).  The following dataframe image contains this information:

![reviews](https://user-images.githubusercontent.com/107599510/197059791-4bd716ca-0ba1-4cbf-b082-a4a22e2fbcb6.png)

#### How many Vine reviews and non-Vine reviews were there?

For this product category, there were a total of 334 vine reviews and 61,614 non-vine reviews.  The total number of reviews for this product equaled 61,948 which breaksdown to 0.54% vine reviews and 99.46% non-vine reviews.  

#### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

In total, there were 32,804 5 star reviews for the products.   From an overall standpoint, that means that 52.95% of total reviews recieved were 5 star reviews. Of the total number of 5 star reviews, 139 were vine reviews while 32,665 were non-vine reviews. This breaks down to vine revies account for 0.42% of total 5 star reviews while non-vine reviews account for 99.58% of total 5 star reviews.

#### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

The total number of vine reviews were 334 and 139 of them were 5 star reviews.  This equates to 41.62% of total vine reviews that were 5 star.  The total number of non-vine reviews were 61,614 of which 32,665 were 5 star reviews.  This equates to 53.02% of total non-vine reviews

## Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.

There does not appear to be positivity bias for this product category for reviews in the vine program.  One would expect to see over 50% 5 star reviews if there was positivity bias and for this analysis, 41.62% of total vine reviews were 5 star reviews.

This data set is filtered by reviewers that had 20 or more total votes and then filtered by reviewers that had 50% or greater helpful votes from their total votes.   One way to test a little further would be to change those parameters.  I ran the test again and changed the reviewer total vote count from 20 to 10 to increase the size of the reviewer pool.  I also lowered the 50% of helpful vote requirement to 40% to add more reviewers to the analysis.  The results were as follows:

![extra_review](https://user-images.githubusercontent.com/107599510/197073281-4a1aec8a-092f-4c8a-98da-a2e0cff3dc01.png)

The total number of reviews increased from 61,948 to 154,344.  The total number of vine reviews increased from 334 to 635 and total vine 5 star reviews increased from 139 to 262.  The total number of non-vine reviews increased from 61,614 to 153,709 and total non-vine 5 star reviews changed from 32,665 to 78,838.  With this increase in reviews for all categories, the percentage of 5 star vine reviews lowered from 41.62 to 41.26%.  Not a massive change, but with increased data, the percentage changed lower to further support that there is not any positivity bias for this particular set of reviews.
