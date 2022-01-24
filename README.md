# HyperionDev-Task-20

This project is Task 20 of level 3 of the hyperionDev Data Science bootcamp set of tasks.
This is the final task of the bootcamp.

This is a Capstone Project and is about a basic form of Natural Language Processing (NLP) - Sentiment Analysis. For this project/task I was required to use a recurrent neural network in Keras to classify book reviews as either positive or negative

The purpose of this project is to teach our neural network to recognise the distinction between negative and positive reviews and be able to classify each review correctly.
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




what the purpose of the project is,
○ what data is being analysed (add links to the datasets if appropriate),
○ how the data is being analysed (add links to .ipynb files if
appropriate) and
○ what the main findings are (add links to report documents where
appropriate).



The project name.
● A clear, short, and to the point description of your project. Describe the
importance of your project, and what it does.
● A table of Contents to allow other people to quickly navigate especially long
or detailed READMEs.
● An installation section which tells other users how to install your project
locally.
● A usage section that instructs others on how to use your project after
they’ve installed it. Include screenshots of your project in action.
● A section for credits which highlights and links to the authors of your project
if the project has been created by more than one person.


What is this repo or project? (You can reuse the repo description you used earlier because this section doesn’t have to be long.)
How does it work?
Who will use this repo or project?
What is the goal of this project?
