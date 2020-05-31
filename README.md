# Spam-or-Ham-Detector-using-NLP
The mentioned project deals with classifying a bunch of messages obtained from different sources into spam or ham by using basic Natural Language Techniques and Naive-Bayes Classification algorithm. Basically the working of this model can be summarized as it trains on a set of cleaned training data and tested upon an unseen  set of data or Test data which contains random labelled messages as being spam or ham. The output of this model is that the message either being classified as spam (1) or ham (0).

![](images/spamorham.png)

# Source of Dataset
The source of the SMS Phone Messages dataset used in this project is obtained from using a dataset from the UCI datasets (https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection). It is a collection of 425 SMS spam messages which was manually extracted from the Grumbletext Web site. This is a UK forum in which cell phone users make public claims about SMS spam messages, most of them without reporting the very spam message received. The dataset contains 5574 instances of total messages including both ham as well as spams.

# Tools and Libraries Used
1. Jupyter Notebook
2. Pandas Library (for Data Manipulation)
3. Matplotlib (for Visualisations)
4. Seaborn (for Visualisations)
5. NLTK Library
6. sklearn library ( Count Vectoriser and Tf-idf Transformer)

# Methodology
1. The datset is read using pandas, since the dataset is a tab separated file hence we use sep='\t' for reading the file into pandas DataFrame.
2. A function is created to pre-process the text data by removing any punctuations and stop words.
3. We can get a list of punctuations by using string.punctuation and a list of stop words from the nltk library.
4. The cleaned messages dataframe then undergoes tokenisation by utilising CountVectoriser from sklearn which converts the list of strings (tokens) into vectors. This is done because computer can't comprehend general strings.
5. Then we import Tfidf Transformer from sklearn to transform the string vectors by assigning them appropriate weights. This method ensures that all words are not given equal importance in the corpus. Thus, weighing down the frequent terms while scaling up the rare ones.
6. The dataset is finally split into train and test data and through a PIPELINE model, all the above steps are performed on the train data separately.
7. Finally we include the last step of pipeline to perform Naive-Bayes Classification to train our model.
8. Lastly we predict on our Test Dataset and find classification report to check how well our model performs on unseen data in order to predict whether a message is spam or ham.

# Conclusion
Hence, the Spam or Ham detector using NLP is successfully implemented and reasonable amount of accuracy is obtained.
