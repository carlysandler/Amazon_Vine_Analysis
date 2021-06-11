# Amazon_Vine_Analysis
---
Analysis of Amazon Product Reviews (Paid Vine Program): Big Data `ETL`  with `PySpark` ,`Python` &amp; `SQL`

## CHALLENGE OVERVIEW
---
This project demonstrates the effective process of Extracting, Transforming and Loading a large dataset. Utilizing PySpark, Postgresql, and an AWS RDS server, has given me the tools to efficently analyze Amazon's Apparel department reviews. The ETL process was a precussor to determining if there is any bias towards favorable reviews from members of the paid Amazon Vine program. 

Bias determination is necessary to weigh the reliability of positive reviews on categorical items. Companies pay Amazon a small fee to provide products to the Amazon Vine members in return for a required review published on the product. If company's rely on these product reviews to strategize future action items, it is important to ensure that these reviews are actually reflective of the product, by isolating the reviews published by "marketing dollars" vs those driven organically. 

We will determine bias by iteratively narrowing into our dataset to filter for only helpful reviews, based on a minimum count of total votes and the proportion of helpful votes compared to the total for an indiviual product. Once the paid vs non-paid reviews are identified, we will compare each groups review count in respect to the number of 5-star reviews.

## FEATURES AND DATA SOURCES
---
- Data Source: "https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Apparel_v1_00.tsv.gz"`
- 
- Programming Files: `challenge_schema.sql`, `Amazon_Reviews_ETL.ipynb`, `Vine_Review_Analysis`
-  Data Tools: `Pandas`, `PySpark`, `Postgresql`, 
-  Software: Google Collaboratory, Python 3.9.2, PgAdmin, AWS RDS 

## CHALLENGE DELIVERABLES
---
Deliverable 1: Perform ETL on Amazon Product Reviews
Deliverable 2: Determine Bias of Vine Reviews
Deliverable 3: A written report on the Analysis (README.md)

## RESULTS
---
1. _How many Vine reviews and non-Vine reviews were there?_

2. _How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?

3. _What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?_


## SUMMARY OF FINDINGS
---

- _Recommendations for Further Analysis_
Although the analysis displays no evidence of positivity bias for reviews in the Vine program, we must delve further into the dataset to provide more analyses or zoom out to our original dataset to amplify our findings against the non-preprocessed and filtered data. For example, I would like to see the spread of total reviews and helpful reviews for each star rating. Right now, we are only viewing 5-star vs the balance of reviews. We can create a frequency dataframe of vine reviews vs non-vine for each star value (1,2,3,4,5) against the total reviews to drill further down into the data. I would use this data to create a summary statistics dataframe and plot each group's distribution of stars given to see if there is visual confirmation of skewness which would reflect bias.

 
