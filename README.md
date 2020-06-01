# WeRateDogs-Twitter-Archive-Account

## Introduction
The project wrangled the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets. The ratings almost always have a denominator of 10, and the numerators almost always greater than 10. The wrangling of this dataset consistes of three parts (gathering, assessing and cleaning)


### 1) Data Gathering


#### The data was gathered from 3 sources:
* The WeRateDogs Twitter archive, which is downloaded manually from Udacity server
* The tweet image predictions, which is downloaded programmatically using the Requests library with given URL
* The dataset of each Tweet Json data (retweet_count and favorte_coun) is gathered by using Tweepy to query Twitter's API

### 2) Data Assessing

The datasets were assessed to inspect for two things: data quality issues (i.e. content issues) and lack of tidiness (i.e. structural issues). Eight quality and 2 tidiness issues were found:

#### Quality Issues

* The timestamp column is in string format.
* Columns(“in_reply_to_status_id", "in_reply_to_user_id", "retweeted_status_id", "in_reply_to_user_id", "retweeted_status_id", "retweeted_status_user_id", "retweeted_status_timestamp) have many missing values. reply and retweeted columns will not be used.
"expanded_urls" varaible has missing values, which means some tweets have no images.
* Some dogs’ names are capitalize and other not.
* Incorrect some dog names.
* Some values of ‘rating_denominator’ != 10.
* Some values of 'rating_numerator' are incorrect.
* Missing values in 'name' = 'None'

#### Tidiness Issues
* There are 4 columns for dog "stage" (doggo, floffer, pupper, and puppo) in the "twitter_archive_df"
* We have 3 different datasets 'tweet_info','image', and 'twitter_archive_df'


#### 3) Data Cleaning

#### The project performed three programmatic data cleaning process:
* Define: convert the assessments into defined cleaning tasks
* Code: convert those definitions to code and run that code.
* Test: test the code to make sure the cleaning operations worked.