# deep-learning-challenge

## Overview of the analysis: 
I was hired by Alphabet Soup, a non-profit foundation, to help determine which project application to fund by analyzing the project probability of success. To do so, I utilize machine learning and neural networks to analyze the Alphabet Soup dataset and create a binary classifier to predict whether applicants' projects will be successful or not, which will help Alphabet Soup to allocate their funding.

## Analysis Results: 

**Data Preprocessing**

### What variable(s) are the target(s) for the model?
The model target, in other words, what the model is trying to predict, is to determine if the project 'IS_SUCCESSFUL' or not. This is represented by the variable y_train under the model coding, which will provide a binary answer = Yer or No.

### What variable(s) are the features for the model?

The features, in other words, what information I am using to answer the target question, under the dataset provided are: 
- EIN: An identification number for each organization.
- NAME: The name of the organization.
- APPLICATION_TYPE: The type of application submitted by the organization.
- AFFILIATION: The affiliation status of the organization.
- CLASSIFICATION: The classification code of the organization.
- USE_CASE: The use case category of the organization.
- ORGANIZATION: The organization type.
- STATUS: The status of the organization.
- INCOME_AMT: The income amount of the organization.
- SPECIAL_CONSIDERATIONS: Indicates if the organization has any special considerations.
- ASK_AMT: The amount requested by the organization.

### Variable(s) removed from the input data because they are neither targets nor features?

Neither, EIN or Name, are useful variables, meaning, they are not relevant in helping to determine if the project would be successful or not; therefore, it was dropped. 

### Compiling, Training, and Evaluating the Model(s)

I created 4 different models to try to find the most reliable one, the results are as follow:

*1st Model - Deep_learning_Code.ipynb Code:*

It resulted in an accuracy score of 70.05% under the test and 95% under the train. This means that under the test it can predict if the project is more likely to succeed by 70%; however, I have more work to do in try to identify why under train I have over 95% accuracy and under test I only have 70.05%. 

The hyperparameters used were:

layers = 2
layer1 = 80 neurons : activation function = ‘relu’
layer2 = 30 neurons : activation function = ‘sigmoid'
epochs = 100

*2nd Model - AlphabetSoudCharity_optimization1.ipynb Code:*

It resulted in an accuracy score of 79.6% under the test and 97% under the train. This means that under the test it can predict if the project is more likely to succeed by 79%; however, I have more work to do in trying to identify why under train I have over 97% accuracy and under test I only have 79.6%. 

The hyperparameters used were:

layers = 2
layer 1 = 80 neurons : activation function = ‘sigmoid’
layer2 = 30 neurons : activation function = ‘sigmoid'
epochs = 10 (Colab kept crashing for anything above 10, even after I restart the running time)

*3rd Model - AlphabetSoudCharity_optimization2.ipynb Code:*

It resulted in an accuracy score of 76.10% under the test and 97% under the train. This means that under the test it can predict if the project is more likely to succeed by 76.10%; however, I have more work to do in trying to identify why 6.under train I have over 97% accuracy and under test I only have 76.10%. 

The hyperparameters used were:

layers = 2
layer 1 = 50 neurons : activation function = ‘relu’
layer 2 = 10 neurons : activation function = ‘tanh'
epochs = 10 (Colab kept crashing for anything above 10, even after I restart the running time)

*4th Model - AlphabetSoudCharity_optimization3.ipynb Code:*

It resulted in an accuracy score of 55.76% under the test and 97% under the train. This means that under the test it can predict if the project is more likely to succeed by 55.76%; however, I have more work to do in trying to identify why 6.under train I have over 97% accuracy and under test I only have 55.76%. 

The hyperparameters used were:

layers = 3
layer 1 = 80 neurons : activation function = ‘relu’
layer 2 = 50 neurons : activation function = ‘sigmoid'
layer 3 = 30 neurons : activation function = ‘sigmoid'
epochs = 10 (Colab kept crashing for anything above 10, even after I restart the running time)

## Summary

In summary, although the train accuracy in all 4 models was over 95%, I can discard model 1 and model 4 as the test accuracy was below 75%. I do have more work to do under model 2 and 3, they do provide a test accuracy of over 75%; however, I need to understand what is causing the variance between the train and the test accuracy. Things I will have to consider:
- Was my model too complex? Did I add too many layers or maybe too many units (neurons)
- Did I choose the right metrics? Did I select the right features for my analysis (info listed above)




