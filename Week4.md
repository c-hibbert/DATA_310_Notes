# Week 4 

# July 28 2020

### Word Embeddings

## Question 1
* Why is using one-hot encoding inefficient towards vectorizing a corpus of words?  How are word embeddings different? (see this video https://www.youtube.com/watch?v=EEk6OiOOT2c)
	* One-hot encoding is inefficient towards vectorizing a corpus of words because it only uses zeroes and ones to denote its differences in words instead of number popularity/position. This can account for long strings of numbers in order to vectorize simple associations, which can be cumbersome. 

## Quesiton 2
* Compile and train the model from the tensorflow exercise.  Plot the training and validation loss as well as accuracy.  Post your plots and describe them.
	* In the plots below, our aim is to train a set of IMDB review

![](word_embedding_tv_acc.png)

![](word_embeddings_tv_loss.png)


### 