# amazon_vine_analysis


### Overview and Purpose:
Using PySpark, the Amazon pet product reviews dataset was extracted and transformed for analysis. A connection to an AWS RDS instance was then established to enable the transformed data to be loaded into pgAdmin tables. PySpark was then utilized again to determine if there is any bias toward favorable reviews from Vine members.

### Analysis Results and Challenges:
Analysis Results
Using PySpark, an analysis was performed on the Amazon pet products reviews dataset (containing 2,643,619 total reviews). The dataset was initally filtered for reviews that obtained at least 20 votes. For this analysis, 20 helpful votes is deemed the minimum criteria to focus the dataset. This filtered dataset was then further filtered to only contain reviews where the number of helpful votes is at least 50% of the total votes for that review. The resulting 38,010 reviews are analyzed to determine if there is any bias towards reviews that were written as part of the Vine program. The following was found associated with the Vine reviews contained within the dataset:

How many Vine reviews and non-Vine reviews were there?
For the 38,010 reviews in the dataset, 170 reviews were associated to the Vine program (paid review) while 37,840 reviews were not part of the Vine program (unpaid review).

How many Vine reviews were 5-stars? How many non-Vine reviews were 5-stars?
Of the 170 Vine reviews, 65 were 5-star reviews. And of the 37,840 unpaid, non-Vine reviews, 20,612 were 5-star reviews.

What percentage of Vine reviews were 5-stars? What percentage of non-Vine reviews were 5-stars?
Based on the total number of paid Vine reviews, 38.2% were 5-star reviws. And based on the total number of unpaid, non-Vine reviews, 54.5% were 5-star reviews

### Vine Review Data Counts
![VineReviewCounts](https://user-images.githubusercontent.com/63277310/130376508-e8184791-7d9d-4562-ab22-8bcd55be6665.png)


# Summary:
Based on the 5-star reviews percentage breakdown alone, there is no positivity bias for the Vine program reviews as there were only 38.2% 5-star reviews associated with paid Vine reviews but 54.5% 5-star reviews associated with unpaid, non-Vine reviews. The number of unpaid reviews compared to paid reviews (significantly larger population size) supports that the percentage breakdown is a reliable indicator and not inappropriately skewed from the smaller total number of paid reviews.

Additional analysis can be performed using Natural language processing (NLP) to perform sentiment analysis on the Vine reviews. This would provide more insight into the sentiment associated with the product reviews to determine if the Vine program contributes to any bias toward favorable reviews from Vine members or if the Vine reviews are sincere and honest 5-star reviews regardless of payment. Associating the 5-star reviews to particular products and then breaking down paid vs. unpaid reviews for each product would also provide evidence on if there was favorable review bias for Vine members or a general customer 5-star satisfaction with the product regardless if the review was paid or unpaid.
