# Amazon Vine Analysis

## Overview
The purpose of the Amazon Vine Analaysis was to analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this anaylsis, we analyzed a dataset containing reviews of video games. PySpark was used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. PySpark was also used to determine if there is any bias toward favorable reviews from Vine members in the dataset. 


## Results
The analysis resulted in the following two DataFrames:

1. The Paid Vine Reviews DataFrame
![vine_paid_df](/Resources/Images/vine_paid_df.png)

2. The Unpaid Non-Vine Reviews DataFrame
![vine_unpaid_df](/Resources/Images/vine_unpaid_df.png)

After analyzing these two DataFrames, the following metrics were calculated.

### Total Number of Vine and Non-Vine Reviews
* Total number of paid Vine reviews: 94
* Total number of unpaid non-Vine reviews: 40471

### Total Number of Vine and Non-Vine 5-Star Reviews
* Total number of paid Vine 5-star reviews: 48
* Total number of unpaid non-Vine 5-star reviews: 15663

### Percentage of Vine and Non-Vine 5-Star Reviews
* Percentage of paid Vine 5-star reviews: 51.06%
* Percentage of unpaid non-Vine 5-star reviews: 38.70%

## Summary
The analysis demonstrated that there is positivity bias for reviews in the Vine program. Since 51.06% of 5-star reviews were part of the Vine program (paid), and only 38.70% were not part of the Vine program (unpaid), it is clear that there was bias in the positive reviews.

An additional analysis that could be performed on the dataset to support this positivity bias is to analyze the number of verified purchase for Vine and non-Vine reviews. This would further verify whether or not positivity bias exists.
