# Author Profiling

This project was done using data from the competition "Author Profiling - Gender identification in Twitter - PAN @ CLEF 2018" (https://pan.webis.de/clef18/pan18-web/author-profiling.html). The focus on the competition is gender identification in Twitter, where text and images may be used as information sources. The training dataset contains 300000 tweets text and 30000 images shared in tweets from 3000 users (100 Tweets text / 10 Images per user). The task is to predict whether the user is male or female, using the text from the tweets, the images or both.

# Using only text

## Features and model for the text

For features were used word and character n-grams, and LSA was used for dimensionality reduction.
Logistic Regression and LightGBM were used, as the Logistic regression gave better results.

## Best result

The accuracy achieved on the test set provided by the competition's organizers is 82.21%.

# Using images only

## Model
For the building of the model was tried various pretrained CNN nets (Xception, MobilNetV2, VGG19). For faster training, the output of the pretrained nets was computed prior the training.
In the end VGG19 was for 'base', due to its smallest shape of the output tensor. Because there was 10 images for every user, keras TimeDistributed layer was used, in order to take into the account all the images at once.

## Best result

The accuracy achieved on the test set provided by the competition's organizers is 71.57%.
