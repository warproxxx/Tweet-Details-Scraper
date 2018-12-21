# Tweet Details Scraper

When you extract live tweets from twitter, the amount of likes, retweets and favourites we receive is 0. Later to find out which of these tweets got succesful we can use this repository to extract details.


This is based on https://github.com/taspinar/twitterscraper but adds multithreading for faster speed and features to extract tweet details for given ID. It bypass limits posed by twitter API.

**Instructions:**

1) Add the required id's in scrape_me.csv
2) Run the program

`python3 scrape_data.py`

Details of given tweets is extracted in the following format:

| ID | Tweet | Time | User | Likes | Replies | Retweets | in_response_to | response_type
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: 
| The ID of the tweet | The tweet text. Contains retweeted and quoted information too if they exist | Unix timestamp of the tweet in UTC Time | Username of the use who posted the tweet | Total number of likes the tweet has received till now | Total number of replies the tweet has received till now | Total number of retweets the tweet has received till now | ID of tweet in whose response the current tweet was made. None if it's a parent tweet | "tweet" or "retweet" or "quoted_retweet"