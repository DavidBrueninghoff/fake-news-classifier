READ ME

###########Fake News Detector (DL) with the ANVIL web application

The Fake News Detector is a model-based application capable of predicting whether information on 
Covid 19 is false or true.


############Features
Insert a full sentence related to COVID-19 vaccinations.Get a prediction if statement is true or false.

############# User guide

The detection of false information was also done with a machine learning model in a parallel work. An 
instruction manual for the Anvil application based on the machine learning model is available here :  
        
https://github.com/yannick5000/Fake-News-Detector-Covid-19-Vaccine/blob/main/README.md

############# Dataset

The data was collected by the team. It was a question of recovering real and false information on reliable 
sites disclosed on the internet. Sentences have been categorized as true or false in an Excel document. In 
the end 1000 sentences were collected to train the model.


############# Data Preprocessing

First, we install the library:
####pip install tensorflow
####!pip install wordcloud
Next, let’s import the library and read in the data:
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
...
from google.colab import drive
drive.mount('/content/drive')
df = pd.read_csv("/content/drive/MyDrive/Fake News Tracker/statements.csv", index_col="Index")

The preprocessing phase consists of cleaning the data. Remove punctuation that could interfere with 
data analysis, remove unnecessary spaces and lowercase the sentences.

###from collections import Counter

nltk.download("stopwords")
stopWordsGerman = stopwords.words("german")
len(stopWordsGerman)  #232 words

Then, we analyze the frequency of each word. Words commonly called "stopword" which come up often 
and have no use for understanding sentences are removed.The lemmatization function allows you to 
contract words and group them into categories.
 eg:Lemmatization -> ‘Care’ ‘Caring’ 


##############  The LSTM model: an improved RNN
LSTM, for Long Short-Term Memory, is a type of RNN widely used in natural language processing.


###############   Split the data into training, test and validation:

In Deep learning, a common task is to study and build algorithms that can learn and make predictions 
about data. Three datasets are commonly used at different stages of model building: Training, 
Validation, and Testing sets.
To see how to split a dataset to train, test, and validation sets with SK Learn?

https://towardsdatascience.com/how-to-split-data-into-three-sets-train-validation-and-test-and-why-e5
0d22d3e54c

###############   Build the model and improve it with hyperparameters:

from tensorflow.keras import layers
model = keras.models.Sequential()
model.add(layers.Embedding(num_unique_words, 32, 
input_length=max_lenght))model.add(layers.LSTM(64, dropout= 0.1))  #dropout 0.3?
model.add(layers.Dense(1, activation = "sigmoid"))  # sigmoid: 2 outpout 0 and 1
model.summary()

Depending on the type of data used and the size of these, there are many specific parameters such as 
layers, dropout, activation .... These parameters can be modified to improve the model. Here you will 
find the 10 most important parameters and their definitions.

https://medium.com/geekculture/10-hyperparameters-to-keep-an-eye-on-for-your-lstm-model-and-o
ther-tips-f0ff5b63fcd4

##########    Support
If you need support or if Google Colab or the interface on Anvil are not working, you can contact one 
of the following people via our TechLabs Slack community:
Arnelle Nguefang Tchouamo
David Brüninghoff
Dora Hinderer
Leïla Mehulić
Mona Fromm
Yannick Reinhardt

