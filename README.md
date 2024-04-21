# Unsupervised_Machine_Learning_Project


Problem statement : Most of the people rely on the search engines to retrieve and share information from various resources. All the results returned by search engines are not always relevant as it is retrieved from heterogeneous data sources. Moreover any user can find it difficult to confirm that the retrieved results are significant to the user query.Therefore semantic web plays a major role in interpreting the relevancy of search results. By using regular keyword search, a document either contains the given word or not, and there is no middle ground. On the other hand, “Semantic Search” can simplify query building, because it is supported by automated natural language processing programs i.e. using Latent Semantic Indexing — a concept that search engines use to discover how a keyword and content work together to mean the same thing. In this project , we will retrieve relevant movie titles using semantic search based on the concept of Natural Language processing (NLP).


We have taken movies dataset , in which we have movie rank, title,	genre,	wiki_plot,	imdb_plot columns

We loaded the dataset , cleaned the data

Then Data Preprocessing was done. The purpose is to remove any unwanted words or characters which are written for human readability, but won’t contribute to topic modelling in anyway.

In the next step we have built the vocabulary of the corpus in which all the unique words are given IDs and their frequency counts are also stored. We have used gensim library for building the dictionary. In gensim, the words are referred as “tokens” and the index of each word in the dictionary is called ID.

Then we did Feature extraction: The doc2bow method of dictionary, iterates through all the words in the text, if the word already exists in the corpus, it increments the frequency count, other wise it inserts the word into the corpus and sets it frequency count to 1

Data Modeling: Tf-Idf means, Term frequency-Inverse Document Frequency. it is a commonly used NLP model that helps you determine the most important words in each document in the corpus. Once the Tf-Idf is build, pass it to LSI model and specify the num of features to build. Latent Semantic Analysis (aka Latent Semantic Indexing): It implements fast truncated SVD (Singular Value Decomposition) to reduce the dimension of the matrix and gives us latent themes.

Now that we have fitted the model , with the index of movies initialized and loaded, we can use it to find similar movies based . When we will input a search query and model will return relevant movie titles with “Relevance %” which is the similarity score. The higher the similarity score, the more similar the query to the document at the given index.

Conclusion: In general usage, computing semantic relationships between textual data enables to recommend articles or products related to given query, to follow trends, to explore a specific subject in more details. In this project the basic version of semantic search was implemented. There are many ways to further enhance it using newer deep learning models.
Use Cases of Semantic Search:
1. Netflix Recommendation System
2. Google Search Engine

References: 
https://zhang-yang.medium.com/semantic-product-search-badcb9b04d7f#:~:text=Unsupervised%20Semantic%20Search,Word%20Embeddings%2C%20and%20Product%20Embeddings

https://dl.acm.org/doi/10.1145/2505515.2505665

https://en.wikipedia.org/wiki/Latent_semantic_analysis#:~:text=Latent%20semantic%20indexing%20(LSI)%20is,an%20unstructured%20collection%20of%20text.

https://www.oncrawl.com/technical-seo/what-is-latent-semantic-indexing/

https://www.geeksforgeeks.org/understanding-tf-idf-term-frequency-inverse-document-frequency/

https://analyticsindiamag.com/singular-value-decomposition-svd-application-recommender-system/
