# Amazon Vine Analysis


## Overview

The purpose of this analysis was to determine if paid Vine Reviews presented a bias compared to unpaid Non-Vine reviews.  This was done using PySpark along with an Amazon Reviews dataset.  The dataset for Lawn & Garden reviews was used.  Below are the highlights and images of the analysis, along with a conclusion based on the results.  

## Results
The first step for transforming the data was to select columns related to reviews and create a new DataFrame.  Next, a new DataFrame was created which only had rows where the number of Total Votes was greater than or equal to 20, to make sure then number of reviews for an item was significant.  Then, a DataFrame and a new column were created to show the ratio of Helpful Votes to Total Votes.  This was filtered further to take out rows where the ratio was under 50%, in order to make sure the remaining data had mostly helpful reviews. 

The final two DataFrames created separated Vine Reviews and Non-Vine Reviews.  The analysis below was done on these two DataFrames to determine if there was a positivity bias for Vine Reviews.

## Vine/Non-Vine Analysis

### Total Vine Reviews
- By using the ".agg" and "sum" functions on the "total_votes" column, then using ".collect" we get the total number of Vine Reviews:  **26195**
![Vine Total](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/vinetotal.PNG)

### Five-Star Vine Reviews
- By using the ".filter" function to get Five-Star Reviews and chaining the ".agg" and "sum" functions, then using ".collect" we get the total number of Five-Star Vine Reviews:  **11558**
![Vine Five Star](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/vinefivestar.PNG)

### Ratio of Five-Star Vine Reviews
- By dividing the "vine_five" list by the "vine_total" list we get th ratio of Five-Star to Total Vine Reviews:  **0.44**
![Vine Ratio](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/vineratio.PNG)

### Total Non-Vine Reviews
- The same method as above was used on the Non-Vine data to get the total number of Non-Vine Reviews:  **2735208**
![Non-Vine Total](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/novinetotal.PNG)

### Five-Star Non-Vine Reviews
- The same method as above was used on the Non-Vine data to get the number of Five-Star Non-Vine Reviews:  **1338327**
![Non-Vine Five Star](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/novinefivestar.PNG)

### Ratio of Five-Star Non-Vine Reviews
- The same method as above was used on the Non-Vine data to get the ratio of Five-Star to Total Non-Vine Reviews:  **0.49**
![Non-Vine Ratio](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/vineratio.PNG)

## Summary

Based on the analysis above, there is no apparent positivity bias for the paid Vine reviews.  Vine reviews had 44% Five-Star Reviews whereas Non-Vine reviews had 48% Five-Star Reviews.  We could possibly conclude that the nature of the Vine reviews (being paid) did not influence a positive rating.  

Further analysis could include Four-Star reviews as well as a breakdown of each star level to see how reviews were distributed overall.  It is possible that, while the ratio of Five-Star reviews is lower for the Vine reviews, there could be a higher ratio of Four-Star reviews, which may indicate a bias.  Additionally, the number of Non-Vine reviews far exceeds the number of Vine reviews in this dataset.  With a more evenly distributed sample, it is possible that the results could change.  

To go even further with the analysis, we could compare different datasets by the type of item they represent.  Lawn & Garden items may not show a bias, but other categories may show a different trend.  This could help us understand the overall impact of the Vine program.

