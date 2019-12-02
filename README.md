# topic_modelling using Word2Vec and Doc2Vec
an algorithm using word embeddings to extract major themes and subthemes in the comments.

Build Date: 09/11/2019
Build Author:Shivendra Singh

# Objective
Survey comments are a major source for a customer experience consulting firm to understand the most significant issue's faced by their client's customers. These comments are analysed manually and tagged to extract three major components :
1. Themes
2. Subthemes
3. Sentiment

Upon analysis, these components play a decisive role in building the action plan to be executed in the coming future. Hence, it is very important to have a high accuracy in this process. However, it is a very time consuming process and requires atleast 40-50 manhours/ project on average.
I have created a basic code using _NLTK tools_ to reduce this effort without reducing the accuracy of the process.I have discussed more about the method used in the following section.

#Methodology

1. __Preprocessing Commnets data__ : Including stopword removal,coversion to lower case and removing symbols. 
2. __Extracting Most Frequent Keywords__ : The top keywords were extracted based on frequency under the assumption that the major themes would be related to these words in the space.
3. __Training Word2Vec and Doc2Vec model__ : Corpus of words and sentences was created and fed to the _GENSIM_ word2vec and doc2vec existing models.The hyperparameters were tuned to improve accuracy of word embeddings.
4. __Creating Keyword clusters based on Cosine Distance__ : The closest words to top keywords were bucketed separately to be used as search keywords into the comments dataset and tag the comments baed on the highest matching bucket
5. __Theme tagging and confidence scores__ : Each bucket of keywords was matched with the major keywords extracted from the comment. A separate score was generated for each bucket based on the matching count.Accordingly, the best bucket for each specific comment was selected and a confidence value for that bucket was also assigned to validate the accuracy of the code.

Conclusion : This work reduced the manual work from __40+ hours__ to less than __2 hours__ for a project with __4 to 5K comments__. I am working to increase the efficiency with time using AllenNLP and other tools.





