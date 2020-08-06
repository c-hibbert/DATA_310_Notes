# Week 3

# July 20

## Quesiton 1
* Write a Problem Statement. Introduce your topic, quantify its significance, and describe the problem as a process.
	* Increasing the efficiency of eccommerce on social media applications like Instagram through machine learning. Eccommerce has grown exponentially over the past ten years, and has become vital now more than ever in the age of a worldwide pandemic. 

## Question 2
* Identify and quantify significant obstacles to solving your problem. Demonstrate why your topic is important, and why the obstacles associated with your topic are significant both globally as well as within the context of your selected application. Describe and analyze the complex nature of the process you are investigating, including the system, the environment, agents and networks. Describe and analyze scope, scale and hierarchy of processes and sub-processes. Describe and analyze factors that contribute to quantified obstacles. Describe and analyze process-oriented causes-effect relationships.
	* The obstacles that I may encounter in the process are finding any data that relates closely to my mission statement aside from the Fashion MNIST data. In my research I’ve run into a lot of sources that interact with several different instances where machine learning is incorporated to fashion, but I’m not sure it corresponds to the theme of my project. My topic is especially important as the world of ecommerce has taken over the way most Americans shop (especially in the age of a pandemic).

### Cats and Dogs Data

## Question 1
* Describe your implementation of the cats & dogs exercise. How did you setup the data?	

_The code is as follows_

		model = tf.keras.models.Sequential([
	    tf.keras.layers.Conv2D(16, (3, 3), activation='relu', input_shape=(150, 150, 3)),
	    tf.keras.layers.MaxPooling2D(2, 2),
	    tf.keras.layers.Conv2D(32, (3, 3), activation='relu'),
	    tf.keras.layers.MaxPooling2D(2, 2),
	    tf.keras.layers.Conv2D(64, (3, 3), activation='relu'),
	    tf.keras.layers.MaxPooling2D(2, 2),
	    tf.keras.layers.Flatten(),
	    tf.keras.layers.Dense(512, activation='relu'),
	    tf.keras.layers.Dense(1, activation='sigmoid')
	])
	
	model.compile(optimizer=RMSprop(lr=0.001), loss='binary_crossentropy', metrics=['acc'])


* The data is set up with three major convolutional layers and pooling layers, due to the sheer size of the data. The input shape is reflected by the dimensions we made all of the pictures earlier. For this model, we are sticking with sigmoid activation so that our values will result in decimal numbers between 0 and 1. 

## Question 2
* Which optimizer have you selected, and how might it compare to other possible choices? (have a look at this site -https://towardsdatascience.com/understanding-rmsprop-faster-neural-network-learning-62e116fcf29a)
	* RMSprop as an optimizer is ideal for maintaining the proper weights of the batches of data we’re using  for training without skewing the results. Using RMSprop is best for large quantities of data.

## Question 3
* Describe your selected loss function and it’s implementation. How is it effectively penalizing bad predictions? (have a look at this site - https://towardsdatascience.com/understanding-binary-cross-entropy-log-loss-a-visual- explanation-a3ac6025181a) What is the purpose of the metric= argument in your model.compile() function?(look here - https://keras.io/api/metrics/)
	* The loss function in this case is the binary cross entropy. It penalizes bad predictions by analyizing the popularity of some terms 

## Question 4
* Plot the accuracy and loss results for both the training and test datasets. Include these in your response. Assess the model and describe how good you think it performed

__INSERT PLOTS HERE__

## Question 5
* Use the model to predict 3 dog images and 3 cat images. Upload you images and the prediction. How did your model perform in practice? Do you have any ideas of how to improve the model’s performance?
	* images used: 

