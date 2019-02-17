# Author Profiling

This project was done using data from the competition "Author Profiling - Gender identification in Twitter - PAN @ CLEF 2018" (https://pan.webis.de/clef18/pan18-web/author-profiling.html). The focus on the competition is gender identification in Twitter, where text and images may be used as information sources. In the training dataset there are 100 tweets from 3000 users, and 10 images shared in tweets for each of the 3000 users. The task is to predict whether the user is male or female, using the text from the tweets, the images or both.

# Features and model for the text

For features were used word and character n-grams, and LSA was used for dimensionality reduction.
Logistic Regression and LightGBM were used, as the Logistic regression gave better results.

# Best result

The accuracy achieved on the test set provided by the competition's organizers is 82.21%.

