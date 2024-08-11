# Customer Age Estimation
----
## Description

A chain supermarket is implementing a computer vision system to process photos of customers. Photo capture at the checkout area will help determine the age of customers in order to:

- Analyze purchases and offer products that may interest customers in that age group.
- Monitor the integrity of cashiers when selling alcohol.

We will build a model that can estimate a person's approximate age based on a photo. We have a dataset of photos of people with their ages indicated. This is a regression task, as we will be predicting a continuous value.

## Tools and skills

_keras, CV_

## Steps

1. Data loaded and initial inspection conducted.
2. Exploratory data analysis and data preprocessing performed.
3. Data prepared for model training.
4. Machine learning model trained.
5. Model performance evaluated on the test set.
6. General conclusion made and recommendations provided to the client.

## Results

The model successfully achieved the target MAE of less than 7. The obtained MAE metric value indicates that, on average, the model makes an error of 6.46 years when predicting a person's age from a photograph. The decrease in both Loss (MSE) and MAE on the training and validation sets indicates good model training. The model quickly adapted to the data and learned relevant features for age prediction. This result was achieved using the ResNet50 architecture with additional GlobalAveragePooling2D and Dense layers, as well as the Adam optimizer with an initial learning rate of 0.0003. Data augmentation using the Flip method was applied to the dataset to increase data diversity—mirror images of the photos were created by flipping them horizontally without altering their content. There are some signs of overfitting, as indicated by the difference between the MAE on the training set (3.15) and the validation set (6.46). The use of regularization tools could potentially improve the metric's performance on the test data. Increasing the number of epochs might also enhance the model's generalization ability; currently, the model was trained for 10 epochs. The imbalanced nature of the data—a small number of individuals over the age of 60 in the dataset—may have also negatively impacted the model's performance.