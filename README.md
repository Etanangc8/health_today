# Health Today Application

## Problem Statement

Our team appreciates the opportunity to provide you with this proposal to help determine the future success of your application launch. 

We begin with providing a problem statement: Based on heavy active traffic to 2 subreddit (Reddit) categories, "Food" and "Exercise" which of these would best predict the success of the new health application. 

## Executive Summary

We begin with extracting data through the Reddit Pushshift API on. Data was extracted (scraped) on April 19, 2020, a loop was created to scape the data before that `current-time` of April 19, 2020. We were able to pull a total of 25,000 comments from both the "Food" and "Exercise" subreddits, exactly 12,500 comments per subreddit.

***
*From here forward "comments" will also be referred to as "body", as the two terms will be used interchangeably within this summary. Subreddit comment posts are nestled in the "body" of the html.* 
***

After the data was extracted (scraped) from the API, our team performed the following steps:
* Data Cleaning
* EDA (Exploratory Data Analysis)
* NLP (Natural Language Processing)
* Modeling: Multinomial Naive Bayes, Logistic Regression, TfidfVectorizer, CountVectorizer

During the initial data cleaning there were total of 2,062 duplicates. Duplicates are defined as repetitive comments, for example the different derivatives of "Thank you"; "Thank you!", "Thank you", "Thanks", "Thank you." Duplicates also included items that were `[deleted]`/ `[removed]` by either the submitter or by Reddit. After removal and initial cleaning, both data frames were concatenated (added together) to create one data frame. 

In the NLP phase, we had to parse the text data to transform it to readable data. During NLP further cleaning was completed, html was removed, as well as any characters that are not within the American alphabet (A - Z). 

Multinomial Naive Bayes and CountVectorizer were ran together and provided a score the best score, Training accuracy was 82.02% vs. a Test accuracy at 83.89%. When we ran Logistic Regression and TfidfVectorizer, that model provided a Training accuracy score of 91.99% vs. a Test accuracy score of 88.56%, this score had a better Training accuracy at almost 100%. Although, we did not lean towards this model because it proved to be overfit. Therefore, the Multinomial NB was the better model predictor. 

**Proposal/ Recommendations:**
From these results we infer that the "Exercise" subreddit is the better predictor for the success in your application. If you were to invest in keywords it should go towards "Exercise" rather than "Food". However, there is only a miniscule difference, therefore investing in keywords that are related to "Food" will also be as beneficial. 
 
