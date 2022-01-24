# HyperionDev-Task-20

This project is Task 20 of level 3 of the hyperionDev Data Science bootcamp set of tasks.
This is the final task of the bootcamp.

This is a Capstone Project and is about a basic form of Natural Language Processing (NLP) - Sentiment Analysis. For this project/task I was required to use a recurrent neural network in Keras to classify book reviews as either positive or negative

The purpose of this project is to teach the neural network to recognise the distinction between negative and positive reviews and be able to classify each review correctly.
This task made use of real world data.

This was broken down in the following setps:

1. The dataset
2. Preprocessing the Data
3. Build the Model RNN
4. Train the model
5. Test the Model
6. Predict Something

## The Dataset
In this task, I used a small portion of the Multi-Domain Sentiment Dataset, which contains product reviews from Amazon. The full dataset contains
reviews for products under the categories: kitchen, books, DVDs, and electronics, but I have focused only on reviews for the book category.
There are only two files, positive.txt and negative.txt, that contained the reviews. Each review is associated with a number of fields. The only field
used was the “title” field, which contained the title of each review. This was used to predict the sentiment of each review as is short and to the point. Therefore, making the task much easier.

Some code was already included in the notebook associated with this task to start such as functions to assist with the task and some preliminary preprocessing steps


Each word in the dataset is mapped to a unique number in the vocabulary(text corpus). A word tokeniser takes a sentence and converts it to a sequence of numbers, which map to the relevant words in the vocabulary. Each book review becomes an array of numbers

## Preprocessing the Data

Next, by feeding all the data to neural network all input reviews were made the same length by padding the reviews with zero's. The pad_sequences function was used for this part of the code.

## Building the model RNN

This is where I built the neural network to classify the sentiment. The network starts with a special layer which assists with text classification through embedding using Keras. This required the input text data to be integer coded so that each word is represented by a unique integer format which was achieved through tokenisation in the preprocessing steps. The embedding layer has three arguments. Namely; the input dim, the output_dim and the input length.
The RNN was built based on the following architecture outlined:

The embedding layer
SpatialDropout(0.2)
BatchNormalization()
LSTM(32)
Dense(2, activation='softmax')

## Training and Tuning the model

This is where the model is compiled and trained. The model is compiled by specifying the loss function and optimizer used while training, as well as
all evaluation metrics measured. Over here the optimizer is set to ‘adam’ and the loss function to ‘binary_crossentropy’.

Once the compilation is complete, next is the training process. There are two important training parameters that were specified , namely batch size and the number of
training epochs. Therefore, together with our model architecture, these parameters determine the total training time.


# The network parameters set: 
The set number of epochs to train for were 5 and batch size 10.
Tuned the output_dim hyper-parameter of the embedding layer to 10, 25, 50 and 100. Then, reported on the performance metrics for each value.
Selected the output_dim which gave the best performance on the test set and plotted a graph of both the accuracy and loss of the model while it was training.
These graphs were used to determine the point at which the model starts to overfit or if it has not yet converged. 
Lastly, reported on the performance metrics of the final model

## Made predictions
Finally, a small selection of samples was provided, no other reviews were added to this sample.
The model was then used for to predict. For this, I needed to translate the sentences into the relevant integers and pad where needed.
This allowed me to put it into the model and see whether it predicts if we will like or dislike the book reviews.
The task was completed.





