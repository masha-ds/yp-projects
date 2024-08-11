# Toxic Comment Recognition
----
## Description

An online store is launching a new service. Users can now edit and add to product descriptions, similar to wiki communities. In other words, customers can suggest edits and comment on the changes made by others. The store needs a tool to detect toxic comments and send them for moderation.
We will train a model to classify comments as positive or negative. We have a dataset labeled for toxicity.
Our task is to train the model to achieve an F1 score of at least 0.75.

## Tools and skills

_nltk, tqdm, TfidfVectorizer, LogisticRegression, ComplementNB, LGBMClassifier_

## Steps

1. Data loaded and initial inspection conducted.
2. Data preprocessing performed.
3. Data prepared for model training.
4. Several machine learning models trained
5. Best model selected and its performance evaluated on the test set.

## Results

The best metric on cross-validation was achieved by the logistic regression model with a regularization coefficient of C=4, without automatic class weighting, and using L1 regularization, which penalizes the sum of the absolute values of the weights. Slightly behind in terms of the F1 metric is the LightGBM gradient boosting model, but its training and prediction speed is significantly higher than that of the regression model, making this classifier much less attractive. The ComplementNB model demonstrates incredible training speed, but unfortunately, its cross-validation metric is the lowest and does not meet the client's minimum requirement.

The F1 score of 0.78 on the test data indicates that the model has a good balance between precision and recall, meaning it is effective at classifying comments as positive or negative, fulfilling the client's requirement.

The precision metric measures what portion of the predicted positive results are true positives. For class 0, this means that 97% of all comments predicted as non-toxic are indeed non-toxic. For class 1, it means that 86% of all comments predicted as toxic are truly toxic. Recall shows what portion of actual positive results were predicted by the model. For class 0, this means that the model identified 99% of all truly positive comments. For class 1, it means that the model identified 72% of all truly negative comments.