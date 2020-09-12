# Text and Sentiment Analysis between Oxygen Not Included and RimWorld
## Problem Statement

This project was approached with an audience of gaming investors in mind. The two games being compared here are _Oxygen Not Included_ and _RimWorld_. When gamers have asked what games are similar to _Oxygen Not Included_ (ONI), _RimWorld_ is often suggested and vice versa. This project looks to compare the social media posts using NLP techniques to classify subreddit posts from the **Oxygennotincluded** and **RimWorld** subreddits. This project sets to find whether or not a model accurately predict and classify posts from subreddit users discussing similar games. Secondly, which game has an overall higher sentiment amongst players on social media?

---
## Web Scrape and Cleaning
Reddit's API _pushshift.io_ was used to scrape Reddit posts from the subreddits **Oxygennotincluded** and **RimWorld**. 15,000 posts were scraped from each subreddit for a combined 30,000 posts. After removing posts that were deleted, removed, or over 1,500 words, the total posts used in the dataset for analysis was 16,533.

---
## EDA
During the exploratory data analysis (EDA), data visualizations of the word counts for post titles and the text within the posts were displayed for each of the two subreddits. Using ```CountVectorizer``` visualizations for the first 20 words were created. 

---
## Modeling
For this project, a text transformer, ```TfidfVectorizer```, was used with the classifiers ```MultinomialNB```, ```RandomTreesClassifier```, and ```LogisticRegression```. Out of these classifiers, the following test accuracy scores were observed: 0.9245, 0.8209, and 0.9252. Tfidf vectorizer and logistic regression had the highest accuracy score with 0.9252. This means that about 92.5% of the data is accounted for in this model. A confusion matrix was made to display the classification predictions between the subreddits **Oxygennotincluded** and **RimWorld**.

---
## Sentiment Analysis with VADER
When comparing the compound score using VADER sentiment analysis, it can be seen that the **Oxgyennotincluded** subreddit posts have a much more positive sentiment score than the **RimWorld** subreddit posts. ONI scored about 0.1 higher than _RimWorld_ with scores of 0.165461 and 0.068434, respectively.

---
## Conclusions and Recommendations
In conclusion, as investors who are interested in how well a game is being received by the public, _Oxygen Not Included_ has the most positive sentiments over _RimWorld_ despite the gaming community recommending _RimWorld_ as a similar game to _Oxygen Not Included_ and vice versa. Future comparisons and analytics may delve into gross profits and sales between the two games in addition to this public sentiment analysis.