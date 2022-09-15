
# Fake News Detector (ML)

## Description
Fake News Detector predicts whether an inserted German statement related to COVID-19 vaccinations is true or false.
### Features
Insert a full sentence related to COVID-19 vaccinations.
Get a prediction if statement is true or false.

### Background
The machine learning model is based on a data base that our group has created. We have collected about 500 true and 500 false pieces of information about COVID-19 vaccinations to train our model.
The model is a logistic regression machine learning model.

### Alternative
Our group has also used another model, a deep learning model (based on the same data base). You can find the Fake News Detector based on the Deep Learning Model here: https://github.com/yannick5000/Fake-News-Detector-Covid-19-Vaccine/blob/de98b134b5ad0943f86b0cd2233b63a848c12cac/README%20deep%20learning%20text.txt

## Installation
Open our Google Colab:
https://colab.research.google.com/drive/1pjN8UmgB_ZcMSjfvo8gxFgPqRUdbTY3g
To run the code, you need your own Google account. Please log in and connect the Google Colab Notebook to your account (also click on "Allow").
To open the data used for our model, you need to import the data to your own Google drive. Please create a new folder called "data" within "ColabNotebooks" in your Google Drive with the following path: drive/MyDrive/ColabNotebooks/data/
Upload the file statements.csv into the "data"-Folder.
You can find the data here: https://github.com/yannick5000/Fake-News-Detector-Covid-19-Vaccine/blob/30ae2a39e2f77d11d84cefd843c7145e1abe7398/statements.csv
Now you are ready to run the code from beginning to end.

## Data
To use the Google Colab notebook, you need to upload the file statements.csv to your own Google Drive.
You can find the data here:https://github.com/yannick5000/Fake-News-Detector-Covid-19-Vaccine/blob/30ae2a39e2f77d11d84cefd843c7145e1abe7398/statements.csv

## Usage
After running all the code in Google Colab, you can start using our application on Anvil, the Fake News Detector.
The URL for the application is: https://XGIH7W2J3XZSQW46.anvil.app/3KGXEUN7XDU6WSMTXUMIEWAZ
Insert any short german sentence related to COVID-19 vaccinations and check whether it is true or false with the respective button.
Our model has an accuracy of about 84 percent. Therefore, you might get wrong answers.
We have provided six different demo sentences in German language (three true, three false) that our model will for sure predict correctly as true or false.
Feel free to insert these sentences.

## Explanation of some code
To train our machine learning model, we needed to preprocess our data base. The model cannot read normal German sentences, but rather calculates the frequency the single words appear in the text corpus and in combination with each other.
For example, we set all letters to lower case and removed so-called stop words (common words like articles). We also lemmatized our sentences, that means single words were reduced to its base form or grouped together with other words.
To understand these steps, you can take a look at the provided example sentence. You will see how it changes throughout the preprocessing.

## Support
If you need support or if Google Colab or the interface on Anvil are not working, you can contact one of the following people via our TechLabs Slack community:
Arnelle Nguefang Tchouamo
David Brüninghoff
Dora Hinderer
Leïla Mehulić
Mona Fromm
Yannick Reinhardt
