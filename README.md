# Project fletcher
This project attempts to predict whether a showerthought will be successful or a failure based on the title. I was inspired by browsing reddit.com/r/showerthoughts, and wondering what separated the upvoted posts from those that never got upvoted. My model uses a pre-trained word2vec model from the University of Ghent in Belgium. You can find the paper in which they train their model [here](https://fredericgodin.com/papers/Named%20Entity%20Recognition%20for%20Twitter%20Microposts%20using%20Distributed%20Word%20Representations.pdf). I used the features generated by the word2vec model in a gradient boosting classifier to predict whether a post is successful or not. 

## Important files in repository

* count-vec-models.ipynb - Trains a couple simple bag of words models as baseline models
* model-tuning.ipynb - Tune final model and generate ROC AUC plot on test data
* showerthoughts-clean.ipynb - Initial cleaning of data and LDA topic modeling
* test-time.ipynb - Attempt to add time component to model to increase AUC
* tfidf.ipynb - Try using TF-IDF representation of showerthoughts with clustering to increase model performance
* word-cloud.ipynb - Generate word cloud for presentation using Tableau
* word2vec-viz.ipynb - Create simple matplotlib visualization showing how I embedded documents
* word2vec.ipynb - Embed showerthoughts in 400 dimensional vectorspace and do initial modeling with features

* redditutils.py - Helper functions to clean data, upsample data, and make features using word2vec
