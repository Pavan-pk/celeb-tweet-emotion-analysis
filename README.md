# Celebrity Tweet Emotion Analysis
Analysis of celebrity tweet emotions by using method of clustering and topic generation using SentenceBert embeddings
----
### Dataset used:
* Tweets Dataset - Top 20 most followed users in Twitter social platform https://dataverse.harvard.edu/dataset.xhtml?id=3047332
----
### Preprocessing:
* Filter out all the tweets not in english (language column of dataset is used.
* Removed URLS from all the files.
* Remove Hashtag and @ (just replace # and @ symbol because hashtag and mention could contain contextual info.)
----
### Generating embeddings:
Used Uniform Manifold Approximation and Projection (UMAP) technique to reduce dimension and visualize embeddings

* all-distilroberta-v1 embedding space
![distil_bert](https://user-images.githubusercontent.com/14234116/168375460-434eb34f-1407-4556-948b-0225dfdd9bfa.png)

* all-mpnet-base-v2
![all-mpnet-base](https://user-images.githubusercontent.com/14234116/168375817-67f6d7d2-8e95-4b78-92eb-f7378b68b3da.png)

* We can see all-mpnet-base-v2 Sentence transformer produce embedding with less overlap after dimentionality reduction.
----
### Clustering:
Used **HDBSCAN** technique to generate contextual topic representation (in numbers).
Network graph of celebrity to topics using Gephi software.
![celeb_tweet](https://user-images.githubusercontent.com/14234116/168376822-ec6296de-7348-4a5f-ac34-d0581d2b9c00.png)

----

I tried to extract the topics from the tweet (using unigram model to extract common words in tweet corpus), but it was too generic and did't yield contexts.
