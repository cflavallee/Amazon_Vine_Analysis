# Amazon Vine Analysis


## Overview

The purpose of this analysis was to determine if paid vine reviews show a bias compared to non-vine reviews.  This was done using PySpark along with an Amazon S3 dataset.  I used the dataset for Lawn & Garden reviews.  Below are the highlights of the analysis, along with a conclusion based on results.

## Results
### Total Vine Reviews
- By using the ".agg" and "sum" functions we get the total number of Vine Reviews:  **23979**
![Vine Total](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/vinetotal.PNG)

### Five-Star Vine Reviews
- Number of Five-Star Vine Reviews:  **11558**
![Vine Five Star](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/vinefivestar.PNG)

### Ratio of Five-Star Vine Reviews
- Ratio of Five-Star to Total Vine Reviews:  **0.48**
![Vine Ratio](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/vineratio.PNG)

### Total Non-Vine Reviews
- By using the ".agg" and "sum" functions we get the total number of Non-Vine Reviews:  **2525046**
![Non-Vine Total](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/novinetotal.PNG)

### Five-Star Non-Vine Reviews
- Number of Five-Star Non-Vine Reviews:  **1338327**
![Non-Vine Five Star](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/novinefivestar.PNG)

### Ratio of Five-Star Non-Vine Reviews
- Ratio of Five-Star to Total Non-Vine Reviews:  **0.53**
![Non-Vine Ratio](https://github.com/cflavallee/Amazon_Vine_Analysis/blob/main/Images/vineratio.PNG)

## Summary

Based on the analysis above, there is no apparent positivity bias for the paid Vine reviews.  Vine reviews had 48% Five-Star reviews whereas Non-Vine reviews had 53% Five-Star reviews.  We can possibly conclude that the nature of the Vine reviews did not influence a positive rating.  

Further analysis could include Four-Star reviews as well as a breakdown of each star level to see how reviews were distributed overall.  It is possible that, while the ratio of Five-Star reviews is lower for the Vine reviews, there could be a higher ration of Four-Star reviews, which may indicate a bias.  Additionally, the number of Non-Vine reviews far exceeds the number of Vine reviews in this dataset.  With a more evenly distributed sample, it is possible that the results could change.  

To go even further with the analysis, we could compare different datasets by the type of item they represent.  Lawn & Garden items may not show a bias, but other categories may have different results. 

