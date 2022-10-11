# Amazon_Vine_Analysis

##Analysis Overview
This project analyzes the Amazon Vine program and determines if there is a bias toward favorable reviews from Vine members.\
The analysis uses PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, load the transformed data into pgAdmin and calculate different metrics.\

##Analysis and Results

1-How many Vine reviews and non-Vine reviews were there?
The dataset appears small for Big Data with 145,431 reviews. Only reviews with 20 or more votes where considered for the rest of the analysis leaving 3,342 reviews. Helpful votes were defined as being 50% or greater than the total votes narrowing the list to 1,685 reviews.
Due to the applied criteria, we have a significantly reduced the sample size. In the following 1,685 reviews, there were no reviews that were paid for by the Vine program.
All 1,656 remaining reviews are unpaid Vine reviews.

2A- How many Vine reviews were 5 stars?
As for 5-star unpaid Vine reviews, there were 631 reviews. Attempting to divide by zero, the code would result in a zero division error. 

2B- How many non-Vine reviews were 5 stars?
There are also 0 paid Vine with 5-star reviews.

3A- What percentage of Vine reviews were 5 stars? 
The percentage of 5-star Vine reviews resulted in 37.4%.

3B- What percentage of non-Vine reviews were 5 stars? 
Zero percent of 5 star reviews were non-Vine reviews.

## Summary
Our focus caused the sample size to be constricted to a degree that it was impossible to compare paid and unpaid Vine reviews, the analysis is biased towards unpaid Vine reviews. 
Another indicator is comparing 37% of unpaid, 5-star Vine reviews to 0% paid, 5-star Vine reviews also shows that the unpaid Vine are biased as well.

The starting criteria of 20 likes or the 50% helpful criteria may have been too high, which made the data set too small. Adjustments to these criteria is a first step to reconsidering using this data set. In addition, running the same analysis using datasets from different product categories can provide us with the whole picture of whether reviews made by Vine members are bias.