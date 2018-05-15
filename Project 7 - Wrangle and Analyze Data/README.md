# Project 7 - Wrangle and Analyze Data - WeRateDogs
[CLICK HERE](https://nbviewer.jupyter.org/github/thunderkatzen/DataAnalytics-Nanodegree/blob/master/Project%207%20-%20Wrangle%20and%20Analyze%20Data/wrangle_act.ipynb) to view the `wrangle_act.ipynb` jupyter notebook in nbviewer to see all the Bokeh Visualizations properly rendered.

__Reviewer's Feedback:__
> Hi Dilip,
Your technical, visualisation, and even narrative skills are superb. This project is outstanding, and I will be nominating it for exceptional effort when I submit my review. I couldn't congratulate you more on the exceptional skill and effort you have put into this one- even the reports were drawn up with exquisite quality. It was a pleasure going through your work, thank you!
***

## Overview
This project was part of the data wrangling section of the Udacity Data Analyst Nanodegree program and is primarily focused on wrangling data from the [**WeRateDogs**](https://twitter.com/dog_rates) Twitter account using Python, documented in a Jupyter Notebook.
    For this project, we only wanted original ratings (no retweets) that have images. Not all of the original tweets in the dataset are dog ratings and some are retweets. <br>
    Fully assessing and cleaning the entire dataset would require exceptional effort so only a subset of its issues (eight quality issues and two tidiness issues at minimum) needed to be assessed and cleaned.<br>
    
The tasks for this project were:
- Data wrangling, which consisted of:
  - Gathering data
  - Assessing data
  - Cleaning data
- Storing, analyzing, and visualizing the wrangled data
- Reporting on the data analysis with insights and visualizations

### The Data
1.) **Twitter archive**
WeRateDogs provided their Twitter archive (which included tweets through August 1, 2017) of basic tweet data (tweet ID, timestamp, text, etc.) for use with this project. The "enhanced" csv file provided by Udacity (twitter_archive_enhanced.csv) also contains columns which were extracted programatically such as the rating numerator, rating denominator, dog's name, and dog stages (doggo, floofer, pupper, and puppo). These columns needed to be assessed and cleaned as the extraction process wasn't perfect.

2.) **Image Predictions Dataset**
Udacity also provided a link to `image_predictions.tsv` which was to be downloaded programatically using the `Requests` library. This dataset contained predictions of dog breeds made by a neural network using the images in the tweets.

3.) **Additional data queried from Tweepy API**
The provided Twitter archive lacked some useful information such as *retweet count* and *favorite count*. The tweet IDs from the twitter archive was used to query the Twitter API for each tweet's JSON data using Python's `Tweepy` library. The resulting JSON data of each tweet was stored in a file called ```tweet_json.txt```. I then read the txt file line by line into a pandas DataFrame only including the desired variables: retweet count and favorite count.

### The Files
* **wrangle_act.ipynb** : Jupyter notebook containing all the code for this project.
* **wrangle_report.pdf**: Briefly discuss the wrangling process and future work.
* **act_report.pdf** : Briefly discuss the insights drawn from improved data set.

### Tools & Concepts Used
- Python
- Pandas
- Numpy
- Bokeh
- Regular Expressions