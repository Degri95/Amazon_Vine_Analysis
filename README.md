# Amazon_Vine_Analysis
Analyzing Amazon reviews with PySpark

## Overview
In this project data was analyzed from the Amazon Vine program to see if there was any bias toward favorable reviews from the Vine members. The Amazon Vine program is a service that lets manufacturers and publishers to receive reviews for their products. Companies will pay a fee to amazon and provide products to vine members, who then are required to leave a review. The dataset I used was for **Musical Instruments**. Google Colab and PySpark were used to perform the ETL process and analysis.<br>

[Dataset here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Musical_Instruments_v1_00.tsv.gz)

## Results

The dataset was first filtered to get a more accurate analysis. Below are the following filters applied.
- Total votes column is greater than or equal to 20.
- Percent of Helpful Votes divided by Total votes is greater than or equal to 50%.
After the filters were applied we had a total number of **14,537** votes.

#### How many Vine reviews and non-Vine reviews were there?

- Vine members made up .4% percent of the votes. (60)

![Vine Votes](/Resources/vine_yes_votes.PNG)

- Non Vine members made up 99.6% of the votes. (14,447)

![Non Vine Votes](/Resources/vine_no_votes.PNG)

#### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

- Vine members had 34 out of 60 votes at 5 stars.

![Vine 5-stars](/Resources/vine_yes_5stars.PNG)

- Non Vine members had 8,212 out of 14,447 votes at 5 stars.

![Non Vine 5-stars](/Resources/vine_no_5stars.PNG)

#### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

- 56.67% of the Vine members votes were 5-stars.

- 56.72% of the non Vine members vontes were 5-stars.

## Summary
Looking at the difference between the percentages of the 5-star ratings between the two groups, I would suggest there is not a positivity bias for the reviews in the Vine program. 
There is only around a .05 difference between the Vine and non Vine members. The non Vine members actually had the marginally higher percentage of 5-star ratings. An additional analysis I would reccomend would be to see if there is a difference in the average votes between the two groups. There might not be a huge difference in 5-star reviews but there may be bias with other star reviews. This hypothesis could be rejected if the difference in means were small enough.
