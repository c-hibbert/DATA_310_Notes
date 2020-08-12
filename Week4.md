# Week 4 

# July 28 2020

### Word Embeddings

## Question 1
* Why is using one-hot encoding inefficient towards vectorizing a corpus of words?  How are word embeddings different? (see this video https://www.youtube.com/watch?v=EEk6OiOOT2c)
	* One-hot encoding is inefficient towards vectorizing a corpus of words because it only uses zeroes and ones to denote its differences in words instead of number popularity/position. This can account for long strings of numbers in order to vectorize simple associations, which can be cumbersome. 

## Quesiton 2
* Compile and train the model from the tensorflow exercise.  Plot the training and validation loss as well as accuracy.  Post your plots and describe them.
	* In the plots below, our aim is to train a set of IMDB review for word validation. The following are the plots. AS you can see, the training accuracy is near 100% but the validation accuracy is incredibly unstable, increasing from 80-90% in 4 epochs and then decreasing rapidly after then. The same follows for the loss, with the validation spiking spontaneously and not leveling off. 

![](word_embedding_tv_acc.png)

![](word_embeddings_tv_loss.png)


### Text Classification with an RNN
## Question 1
* Again compile and train the model from the tensorflow exercise.  Plot the training and validation loss as well as accuracy.  Stack two or more LSTM layers in your model.  Post your plots and describe them.
	* In this situation, the additional lstm layers added to the training and validation graphs applied no significant change to the graph's shape. The training and validation accuracy still leveled off at around the same area (on the first to second epoch).

_Without LSTM_
![](training_acc1.png)
![](training_loss1.png)

_With LSTM_

![](training_acc_lstm.png)

![](training_loss_lstm.png)



# July 29

### Using NLP to build a sarcasm classifier
* Pick two or three news sources and select a few news titles from their feed (about 5 is likely enough).  For example you could select CNN, Fox News, MSNBC, NPR, PBS, Al Jazeera, RT (Russia Today), Deutsche Welle, Facebook, BBC, France24, CCTV, NHK World or another source you wish you analyze.  Run your sarcasm model to predict whether the titles are interpreted as sarcastic or not.  Analyze the results and comment on the different news sources you have selected.
* For this classifier, I used the following headliners:
	* from HuffPost: "Big Tech CEOs Answer To Congress On Competition"
		* result- [9.3155913e-03] - "not sarcastic"
	* from Fox News: "Look who's footing the bill for de Blasio's policy of housing homeless in hotels"
		* result- [3.0634948e-07] - "not sarcastic" (although I beg to differ)
	* from Al Jazeer: "COVID-19: New York's true nursing home death toll is likely high"
		* result- [4.7606733e-04] - "not sarcastic"
* I would argue that the filter is inaccurate, although it very well did try. After looking at Huff Post and Al Jazeer's headliners, I would suspect that Fox News' article title would be seen as incredibly sarcastic. According to the classifier, however, that is not the case.


### Text generation with an RNN
* Use the generate_text() command at the end of the exercise to produce synthetic output from your RNN model.  Run it a second time and review the output.  How has your RNN model been able to “learn” and “remember” the shakespeare text in order to reproduce a similar output?

_The following is the Shakespeare text generated after two runs_

	ROMEO: I may at
	Corapiless vial tempisartly,
	I'll do him ashes not the mind of your honour.
	
	PETRUCHIO:
	Who cousins here?
	That stand within the well-comfort in my blow his greeful day: the rest, which bid
	It were the England confusion of des
	Alas, Montague it pleasure sister,
	Thy ends for proud my books. Where is her eye,
	Thene were an edmand great are services stend us.
	
	VIRGILIA:
	I am the king, who have not die to seiz upon thy sword:
	Would the people, of a vilour will shall
	Most sugden his substance as ce
	Our dread soul venture would tell this most self,
	Nor chances after down by what's the port,
	My house of yourselves draw justice
	Murches the buttafforced. Ho must nature,
	Though she would make your design,
	If time my mighty stock sadches wearselfea-need him.
	Would on home. Your aid,
	I go fortain'd for your majesty.
	
	KING HENRY VI:
	For that cannot a high absent born. But why, being love thy hand,
	I will be clofk.

	CLIUF:
	Therefore, buring in death; my girl and thine express, he looks any s

Allowing the RNN to process twice as it goes forward **and** backwards through a bidirectional keras layer allows the input to take in and learn large heaps of information in a timely manner and reiterate the results ina more accurate way. 

### Neural machine translation with attention
* Use the translate() command at the end of the exercise to translate three sentences from Spanish to English.  How did your translations turn out?
