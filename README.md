***Sentiment Analysis of IMDB Movie Reviews***


This project focuses on sentiment analysis of movie reviews using the IMDB dataset. 


**Dataset**

The project uses the IMDB Dataset containing review and sentiment columns.

*Dataset*: https://drive.google.com/file/d/1hyn6U44cvUNedMnzPHzHsiBgXMHFBjBw/view

*Glove.6B.100d*: https://drive.google.com/file/d/1CLrwskD-M8ce0M5agxRjB3OhKuKiCcCn/view 
 


**Data Preprocessing**

*Tokenization*: Reviews are tokenized using Keras’ Tokenizer.

*Padding*: Sequences are padded to ensure uniform input dimensions.

*Label Conversion*: Sentiment labels are converted to binary (positive: 1, negative: 0).


**GloVe Word Embeddings**

A pre-trained GloVe embeddings file (glove.6B.100d.txt)is used to map words to 100-dimensional vectors.


**Sentiment Analysis Models**

*Shallow Neural Network*: Two dense layers with 100-dimensional GloVe embeddings.

*Unidirectional LSTM*: Replaced the first dense layer with a single LSTM layer.

*Bidirectional LSTM*: Enhanced the LSTM layer to process text in both forward and backward directions.


**Model Training and Evaluation**

Batch Size: 32 (optimized through testing).

Epochs: 20.

Metrics: Accuracy and F1 score for both training and testing sets.


**Results**

| Model                 | Training Accuracy | Testing Accuracy | Training F1 | Testing F1 |
|-----------------------|-------------------|------------------|-------------|------------|
| Shallow NN            | 57.16%           | 55.78%           | 0.7136      | 0.6987     |
| Unidirectional LSTM   | 87.96%           | 84.11%           | 0.8724      | 0.8304     |
| Bidirectional LSTM    | 90.98%           | 84.74%           | 0.9068      | 0.8398     |


**Requirements**

Python 3.x

Libraries:

Pandas

Keras (with TensorFlow backend)

NumPy
