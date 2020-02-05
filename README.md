# Classifying_Climate_Change_Tweets
Metis Project 04, Part I  

- This github repo contains a classification project that identifies climate change tweets from 2017–2019 as either "believer" or "denier" tweets. 
- 20 million climate change tweet ID's were downloaded from the [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/5QCCUU) and "hydrated" (i.e. populated with JSON files containing the actual tweet, tweet details, retweet details, user info, etc.) using `twarc`.
- The tweet files were then saved in a mongoDB database, all retweets were filtered out, and the remaining tweets were classified as "believer" or "denier" using hashtags and text processing (see jupyter notebooks for more details). This classification process is part I of an overarching project.  Part II involves topic modeling and clustering of the tweets to identify sentimental trends by geographic location.
- Find an article published on Toward Data Science [here](https://towardsdatascience.com/classifying-climate-change-tweets-8245450a5e96) that walks through the process in more detail.

## Jupyter Notebooks
- "Project_04_Data_All_Tweets"
	- Extracts desired tweets from mongoDB database
	- Organizes tweets into dataframe
	- Cleans up dataframe
- "Project_04_Classifier_R1"
	- Selects "definitive" hashtags
	- Performs text preprocessing on tweets
	- Tests a number of classifier baseline models
	- Performs grid search to optimize best models
	- Classifies entire tweet dataset 