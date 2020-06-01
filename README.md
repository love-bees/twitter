# Sentiment heatmap based on Twitter data on Covid

The code gathers geographical data of Twitter users who made posts related to covid in a select time period and writes it to a CSV file, along with the time it was posted, hashtags and the contents of the tweet.

To get a consumer API key and secret: apply for a developer account on Twitter (takes about a week for them to respond, be patient).

Once that's done, you'll be able to create an app on Twitter, which in turn will give you the access token and secret. Copy all those into the Python code in data_generation.ipynb (you can open it using Colab) and feel free to gather your own.

In the twitter_data_analysis.ipynb file, the data is cleaned up, the language is filtered (English) and it is then parsed through the SentimentIntensityAnalyzer using the Vader lexicon to fetch the sentiment scores. 

Country names are gathered by reverse geocoding from the coordinates gathered.

The mean score is then calculated for each unique country and mapped onto a world map.
