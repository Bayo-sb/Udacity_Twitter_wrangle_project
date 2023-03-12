#WeRateDogs Data Wrangling and Analysis
This is a Data Wrangling and Analysis project completed as part of the Data Analyst Nano Degree program. The dataset used for this project is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. This Twitter account rates people's dogs with a humorous comment about the dog.

The data wrangling process was divided into three stages:

Gathering Data
Assessing Data
Cleaning Data
Gathering Data
The data was gathered from three different sources:

Enhanced Twitter Archive: This data was downloaded manually from the given link and uploaded to the local project work space. It contains information such as dog names, ratings, and dog stage.

Image Prediction File: The Requests Library was used to download this file from the Udacity Servers. This file consists of tweet_id, image url, and three image predictions with their confident predictions.

Twitter API: Twitter API was queried to obtain favorite_counts, retweets_counts with tweet_id obtained from Enhanced Twitter Archive. A Twitter developer account was applied for on the Twitter platform to be able to gather from the Twitter API.

Assessing Data
The data was assessed on two levels: visually and programmatically to pinpoint data qualities and tidiness issues associated with the data.

Tidiness:
doggo, floofer, pupper, puppo columns in twitter_archive_enhanced dataset should be combined into a single column.
Related datasets exist separately.
Quality:
From tweet image predictions dataset:

Underscore used to separate some predicted dog names across p1, p2 and p3 columns.
Some dog names started with lower case while some start with upper case.
Wrong data type assigned to tweet_id column int64 instead of string.
From Twitter API dataset:

Wrong data type assigned to the id column int64 instead of string.
From Twitter Archive Data:

Wrong data type assigned to the timestamp column (object instead of Datetime).
Wrong data type assigned to the tweet_id column (int64 instead of string).
There are 181 retweet values as shown by the retweet_id.
Some rows have rating_denominator values not equal to 10.
Invalid values in the name column.
Cleaning Data
The following operations were done to get rid of quality and tidiness issues raised during the assessment of the data:

Renaming of columns
Extraction of values from text
Changing Data types to appropriate ones
Merging of Datasets
Dropping Columns with high missing values
The cleaned dataset was then used for further analysis and visualization. The code and the report for this project can be found in this repository.

