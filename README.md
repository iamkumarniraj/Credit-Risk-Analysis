UCI Credit Card Dataset

Generalized Concepts For the Project

This dataset contains information about credit card holders, including their demographics, credit history, and payment records. The data was collected from credit card holders in Taiwan from April 2005 to September 2005. The goal of this project is to predict whether a credit card holder will default on their payment based on their demographic and credit history.


The project will consist of four main stages:

Preprocessing the dataset: This involves cleaning the data and preparing it for analysis. This includes handling missing values, dealing with outliers, and transforming variables if needed.

Exploratory Data Analysis: This involves exploring the relationships between different variables and identifying patterns in the data. This can be done using various visualization techniques, such as scatterplots, histograms, and correlation matrices.

Model Testing and Evaluation: This involves selecting and testing different machine learning models to predict default. The models will be evaluated using various metrics, such as accuracy, precision, recall, and F1-score. The goal is to select the best model that can predict default accurately.

Finalizing Model for the Predictions of Defaulter: The final stage involves training the selected model on the entire dataset and using it to predict default for new credit card holders. The model will be saved and can be used to predict default in the future.

Preprocessing the Dataset
The dataset contains 25 variables, including demographic variables such as age, sex, and education, as well as credit history variables such as credit limit, payment history, and bill amount. The dataset also includes a binary variable indicating whether a credit card holder defaulted on their payment in the following month.

The first step in preprocessing the dataset is to check for missing values and handle them appropriately. The dataset should also be checked for outliers, we have kept the outliers in the study as it could have correlation with defaulter. The variables may also need to be transformed to ensure that they are normally distributed or have a similar scale.

Exploratory Data Analysis
Exploratory data analysis involves exploring the relationships between different variables and identifying patterns in the data. In this project, we have used various visualization techniques, such as scatterplots, histograms, and correlation matrices. The objective is to find factors that have a significant correlation to default and can be utilized to precisely forecast default. Additionally, we discovered a number of characteristics that strongly correlate with one another. None of the input variables had a strong correlation with the default variable. We did not exclude any columns from the research as a result.

Model Testing and Evaluation
Model testing and evaluation involves selecting and testing different machine learning models to predict default. The models will be evaluated using various metrics, such as accuracy, precision, recall, and F1-score. The goal is to select the best model that can predict default accurately. Several models have been tested, including logistic regression, decision trees, Gradient Booster, and Support Vector Machine. The models will be trained on a portion of the dataset and tested on another portion to evaluate their performance. The best model will be selected based on its performance on the testing dataset.

Finalizing Model for the Predictions of Defaulter
The final stage involves training the selected model on the entire dataset and using it to predict default for new credit card holders.
Overall, the classification report indicates that the logistic regression model was performing reasonably well, but there wass definitely room for improvement, especially in identifying the defaulters.By using a decision tree classifier, we acheived stark contrast between the accuracy during training and accuracy during testing. The sole reason for this was because decision trees on unbalanced datasets have a tendency to favor the majority class since they divide the data into subsets to optimize information gain without accounting for the distribution of classes. As a result, the resultant tree may be heavily biased in favor of the majority class, which would reduce its ability to forecast the minority class. 
The reports for Gradient Booster indicated that the model achieved an overall accuracy of 0.83 on the training dataset and 0.82 on the testing dataset. The precision for the majority class (0) is high on both datasets (0.84), indicating that the model is able to correctly identify non-defaulters with high accuracy. However, the precision for the minority class (1) is lower (0.70 on training data and 0.66 on testing data), indicating that the model struggles to correctly identify defaulters.
Similarly, for SVC We observed from comparing the classification reports for TrainData and TestData that class 1 has worse accuracy, recall, and f1-scores than class 0 in both instances. Due to the imbalance in the dataset, it is not surprising that the model is not performing well in predicting class 1, or the minority class. The ratings for class 0 are, however, noticeably higher, suggesting that the model is doing a better job of predicting the dominant class. A further sign that the model is overfitting the training data is that the accuracy score of the TrainData is greater than the accuracy score of the TestData. To balance the dataset and enhance the model's performance on the minority class, we must treat the imbalance dataset.
Hence, HyperParameter tuning was performed to increase the accuracy. After the tuning, We selected Decision Tree Classifier on the basis of it's accuracy and other metrics like precision and recall and can be used to predict default in the future.


Decision Tree model is finalized, it can be used to identify credit card holders who are at high risk of defaulting on their payments. This information can be used by credit card companies to manage their risk and avoid losses due to defaults.




