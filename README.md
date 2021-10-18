# Amazon Vine Analysis

## Overview & Purpose
This project required us to take the information from an Amazon Vine dataset, and transform it into a structure that could be added to an existing Postgres database. To acheive this, we used Pyspark to read in the dataset and transform it into 4 dataframes that could be written to the Postgres database using an AWS RDS.</p>
<img src = "https://raw.githubusercontent.com/AlexisBurton/Src-images/master/Screen%20Shot%202021-10-15%20at%2011.44.23%20PM.png">

## Results
To determine if there was any bias with the Vine reviews, we first filtered the data to include only reviews that were voted helpful at least 50% of the time. Using the filtered dataset, we then looked at the total Vine vs non-Vine reviews as well as the percentage of 5-star reviews for each group.
</p>

|  |Total reviews| 5-Star Reviews| % 5-Star Reviews|
|---|---|---|---|
|Vine|47|15|31.91|
|non-Vine|8362|4332|51.81|



## Summary
While the Vine dataset is substantially smaller than non-Vine, it does suggest that there is some bias in the Vine reviews. Since the Vine reviewers are compensated for their reviews, they may feel compelled to be more critical of the item, and therefore less likely to give a 5-star review.