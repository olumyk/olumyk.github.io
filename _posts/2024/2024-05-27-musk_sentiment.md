---
title: "Analyzing Public Perception and topics Surrounding Elon Musk on Twitter"
date: 2024-05-27
categories: [Data Science, Data Engineering]
tags: [aws, azure, twitter API, Apache Spark]
image: 
  path: /assets/images/pro_01/process_flow.png
---

> If you prefer to delve directly into the code, feel free to explore my github repository [here](https://github.com/olumyk/musk_sentiment) 
{: .prompt-tip }



## Introduction

In today's digital age, social media platforms serve as rich sources of data for understanding public sentiment and opinion on various topics
This project focuses on analyzing Twitter data related to Elon Musk, a prominent figure in the tech industry, between November 21 to 22, 2022
The objective is to gain insights into public sentiment towards Elon Musk during this period and extract meaningful topics from the tweets

The following are notable highlights of Elon Musk around November 2022 that may influence the public perception of this iconic figure:
 - Elon Musk confirms plans to charge $8 per month for Twitter verification
 - Elon Musk restored some banned Twitter accounts including that of Donald trump
 - Musk sells nearly $4 billion worth of Tesla stock
 - Twitter's workforce drops to less than half after Musk’s mass layoffs



## Objectives

  - Collect Twitter data containing mentions of Elon Musk
  - Clean and preprocess the collected data
  - Analyze sentiment and derive topics from the tweets
  - Train and evaluate machine learning models to predict sentiment
  - Create a dashboard to visualize insights from the data



## Methodology

  - Data Collection: twitter API is integrated with AWS Data Firehose and S3 bucket via EC2 instance
  - Data Cleaning: the dataset is securely transfered from S3 bucket to MS Azure Databricks for wrangling 
  - Sentiment Analysis: for the NLP, pretrained model from Hugging Face Transformer library is employed
  - Topic Modeling: applied topic modeling algorithms to identify prevalent themes and discussions
  - Feature transformation and Model Training: transformed the tweet to chunks suitable for training and validating ML algorithm
  - Pipeline: pipelines are created for the trained models, and the resulting datasets were exported to a private S3 bucket for further analysis 
  - Visualization and Interpretation: tables are generated from the stored dataset using AWS Athena. The curated data is then visualized QuickSight dashboard



## Outcomes

- Identification of dominant sentiment clusters and key themes emerging from the Twitter data
- Insights into public sentiment towards Elon Musk were gained, revealing a majority of negative sentiments during the specified time period
- Visualization of sentiment trends and topic distributions to facilitate understanding and interpretation of the data

![dashboard](/assets/images/pro_01/dashboard.webp)


## Conclusions

  - Analyst attributed the considerable drop in Tesla’s stock price in 2022 to the involvement of Musk’s with Twitter (business insider, 2022) 
  - The imbalance dataset shown on the dashboard reveals that majority of the sentiments expressed in tweets are negative, which may attest to the analyst statement above
  - There is high chances of predicting the right sentiment of new tweets taking into consideration the 94% accuracy of Logistic Regression classifier

