# TED-Talks-Segmentation-and-Topics-Extraction

TED Talks are knowledge videos of talks by experts in technology, entertainment, and
design (hence TED). These conferences are arranged across the world. Great speakers
come forward and share their experiences and knowledge. These talks are limited to a
maximum length of 18 minutes and cover a wide range of topics. The videos are stored,
and every video has a description of the video content.

# Problem Statement:
There are tons of these videos across the world. They are recorded in different locations,
with different topics and a variety of speakers. Tagging these videos manually to a
certain category is the biggest challenge given the number of videos we have already.
Let’s look at machine learning and natural language processing to solve this
problem.

# About the data:
* considering the open source data for this project.
* The dataset consists of 2467 transcripts(Descriptions)

# Challenges:
we don’t have labeled data to train a classifier and predict
the categories.

# Approach:
* taking the unsupervised learning approach.
* Converting the texts to features by using different techniques
 1) Count-vectorizer
 2) TF-IDF
 3) Word embeddings(word2vec , Glove etc)
 4) SBERT(Sentence bert)-- considered best approach because,
   > The extracted features will be dense embeddings and are not sparse like Count vectors and TF-IDF.
   
   > The extracted embeddings will be the good representation of entire sentence.
* using KMeans clustering to segment the extracted vectors(TED Talks).
* Once the clustering is performed, the next problem is to understand the clusters.
* Then, using topic modeling to extract topics and learn the cluster properties.
