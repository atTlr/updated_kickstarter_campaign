# Kickstarter Campaigns
## June 2023


* Tyler Zarnik Github: atTlr

---

## Problem Statement

In accordance with Kickstarter’s continued efforts to operate as a “Benefit Corporation”,  the company is looking to take a data driven approach to continue to provide information that fosters more successful campaigns from creators on the platform. These data driven insights may be able to help creators understand what successful campaigns are doing right. There is also a desire to have this data predict which campaigns will be successful based on metrics of similar campaigns provided. 

---

## Executive Summary

The primary purpose of this project is to attempt to compile a comprehensive analysis of publicly available Kickstarter datasets with the goal to provide visualizations of the data as well as a machine learning model that will predict and give a probability of if the campaign will be successful.

We will incorporate the python libraries pandas, numpy, and matplotlib for the Data Cleaning and Data Visualization steps of the project. Sklearn will be the library used for the machine learning model. We will be utilizing Amazon Web Services (AWS) to run and return our fitted model. A logistic regression will be used for the explanatory model while a random forest classifier will be used for a more predictive model. Natural Language Processing will additionally be used as further exogenous variables within our modeling pipeline as a way to incorporate the title and description of the Kickstarter Campaign as well.

The analysis will also incorporate current articles that have been pubished by Kickstarter themselves as 'best practices' for running a campaign. We will look to corroborate any of these 'best practices' if they can be shown through the data as well as provide our own reccomendations based on our model.

---

## Table of Contents

- [Preliminary Data On Kickstarter](#Preliminary-Data-On-Kickstarter)
- [Tips Normally Explaining Successful Campaigns](#Tips-Normally-Explaining-Successful-Campaigns)
- [Data Dictionary](#Data-Dictionary)
- [Data Collection](#Data-Collection)
- [Imports](#Imports)
- [Exploratory Data Analysis](#EDA)
- [Preprocessing & Modeling](#Preprocessing-&-Modeling)
- [Evaluation and Selection](#Evaluation-and-Selection)
- [Conclusion and Recommendations](#Conclusion-and-Recommendations)


--- 

## Data Dictionary


|Feature|Type|Dataset|Description|
|---|---|---|---|
|id|object|df|Identifing ID For Each Campaign|
|name|object|df|Name and Description of the Campaign|
|category|object|df|Subcategory Description of the Campaign|
|main_category|object|df|Category Of the Campaign|
|currency|object|df|Currency of Pledged Amount|
|launched|datetime|df|Date When Campaign Was Created and Started|
|deadline|datetime|df|Designated End Date of Campaign|
|pledged|float|df|Amount Pledged In Amount of Currency|
|usd_pledged|float|df|Amount Pledged in US Dollars|
|goal|float|df|Amount That Creator Needs To Complete Project|
|backers|int|df|Number of Users That Have Donated to the Campaign|
|country|object|df|Country In Which the Campaign is Taking Place|
|spotlight|object|df|If The Campaign Was Spotlighted on the Kickstarter Website|
|staff_pick|object|df|If the Campaign Was Endorsed by the Staff at Kickstarter|
|duration|int|df|Length In Days of Kickstarter Campaign|
|month_launched|object|df|Month in Which Campaign Was Launched|
|result|int|df|Whether the Campaign Reached The Goal Set|

---

## Conclusions and Recommendations

Deploy a model that will be able to return the probability that a campaign will succeed based on simple stats such as backer count, duration, title/description, goal, and current pledged amount. With the deployed logistic regression, it can give specific tailored information on best ways to move forward with the strongest coefficients. Incentivize repeat creator projects. Give lower percentages to creators who consistently produce successful campaigns. Work to give more spotlight to newer campaigns and encourage past successful creators to re-engage with the platform with discount percentage incentives.

As revenue for the company is derived directly from the success of its creators, Kickstarter has an incentive to invest in its creators as much as possible. While there are great resources provided by Kickstarter on best practices and beginners info, this info sometimes is not directly tailored to a customer. Creating and deploying a model that is able to give a predicted probability of success as well as identify important features of successful campaigns, will aid new creators to be successful. As seen, creators that have successful campaigns will also be more likely to have future successful campaigns which also often get more pledge USD per campaign.

---

## References

- https://www.kickstarter.com/help/stats?ref=global-footer
- https://www.forbes.com/sites/jaredhecht/2020/08/31/is-crowdfunding-a-good-option-for-businesses-during-the-pandemic/#3184ee5565f0
- https://www.kickstarter.com/charter?ref=global-footer
- https://www.cnbc.com/2014/09/23/the-man-who-made-50-million-ditching-kickstarter.html
