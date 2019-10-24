# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & Classification

# Problem Statement¶
Given the rise in adoption of OTT streaming services, and the launch of newer players in 2019 (e.g. HBO GO, Disney+), the CEO of Netflix is interested in understanding feedback on their streaming service through going through forums where consumers actively discuss the pros and cons of each streaming service, such as the Cordcutters Forum - https://forums.cordcutters.com. However the forums are often not sorted/classified well, and it is time consuming to go through each comment before understanding which streaming service the consumer is referring to. In order to solve this problem, I have decided to train a model to understand what are the key words in comments/posts that consumers typically mention when referring to Netflix through using subreddits /r/netflix and contrast it to /r/hulu, which is the largest competitor of Netflix at this point in time.

# Executive Summary
The model chosen is the Logistic Regression model with a TFIFD vectorizer, which allows a maximum number of 3000 features, and a combination of up to 3 words. This model has been verified to be quite effective at classifying between two subreddits (I had tested the model on two other subreddits /r/MakeupAddiction and /r/SkincareAddiction which are also close in terms of word frequency and terminology and have achieved a great score of 98%) and had achieved an accuracy score of ~93%.

Interesting features to note is that Netflix comments are mostly distinguished through titles of popular shows (e.g. Stranger Things) however what distinguishes Hulu comments are its features (e.g. Live TV, DVR, Commercials).

# Conclusion
The model chosen works well to classify subreddits, not only that of Netflix and Hulu, but other subreddits where the syntax is generally quite close too. I had initially expected the accuracy score to be quite low given the similarities but the Logistic Regression together with a TFIFD vectorizer which allows up to 3 combined words (which will then capture popular title names for the streaming devices/OTT dataset, but didn't really matter when it came to the makeup and skincare dataset).

The model had also managed to capture the key differences in the OTT dataset, which shows through the key features of each dataset, where Netflix comments were differentiated through the titles offered, and Hulu through its features (e.g. commercials, live TV, channels, ability to connect to DVR).
