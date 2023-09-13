# deep-learning-challenge

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

```
    EIN and NAME—Identification columns
    APPLICATION_TYPE—Alphabet Soup application type
    AFFILIATION—Affiliated sector of industry
    CLASSIFICATION—Government organization classification
    USE_CASE—Use case for funding
    ORGANIZATION—Organization type
    STATUS—Active status
    INCOME_AMT—Income classification
    SPECIAL_CONSIDERATIONS—Special considerations for application
    ASK_AMT—Funding amount requested
    IS_SUCCESSFUL—Was the money used effectively
```

## Table of Contents

- [Introduction](#introduction)
- [Dependencies](#dependencies)
- [Preprocessing](#preprocessing)
- [Compile, Train, and Evaluate the Model](#compile-train-and-evaluate-the-model)
- [Optimization](#optimization)

## Introduction

This analysis is designed to predict whether a charitable application will be successful or not for Alphabet Soup. This is done by the model taking in our preprocessed data to make predictions based on the features and variance of the data.

## Dependencies

```
sklearn 
pandas 
tensorflow 
```

## Preprocessing

First, we read the csv into a Pandas DataFrame. After this, we clean up the dataframe to get it ready for the nerual network. This is done by dropping data we may not need such as the EIN and NAME columns. We also bin some of the data and remove outliers.
Pandas then helps us out next by encoding the data with pd.get_dummies. We then assign a train_test_split and scale the data so we can use it in our nerual network.

## Compile, Train, and Evaluate the Model

After we have the data ready, we use the TensorFlow to create our nerual network and establish how many hidden layers and neurons are in our model.  Next we compile the model and train it base off of the data from the preprocessing. Output the results to a file and monitored the model to ensure it's accuracy and loss.

## Optimization

To make the model more accurate, ideally 75%, we must make some changes to the original notebook to make the model more accurate. Below are a list of measures taken to optimize the model to get it working at a final 78% accuracy.

```
- Binned the names in the main dataframe instead of removing them from the table to give the model more data to correlate
- Limited the amount of values in columns where outliers where too large with binning or removing
- Trained on more epochs to ensure results
```

