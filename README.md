# Unit 11 - Risky Business Homework
Unit 11 Machine Learning

This assignment seeks to create financial model using logistic regression classifiers on loan data from LendingClub with the intention of evaluating loan risk.

## I. Dependencies
This project utilizes the following libraries:
* Pandas
* Numpy
* pathlib
    * Imports:
        * path
* collections
    * Imports:
        * counter
* sklearn: 
    * Imports:
        * balanced_accuracy_score
        * confusion_matrix
        * model_selection
        * LabelEncoder
        * StandardScaler
        * RandomForestClassifier
        * classification_report_imbalanced
        * LogisticRegression
        
       
* imblearn
    * Imports:
        * classification_report_imbalanced
        * EasyEnsembleClassifier
        * Metrics
        * RandomOverSampler
        * SMOTE
        * ClusterCentroids
        * SMOTEENN
* Warnings
        


The imbalanced learn library and scikit learn library are used to resample and evaluate data.

## II. Summary of Findings
Given the data from modeling, I believe both models are good models, depending upon what you wanted the models to accomplish. Both have high balanced accuracy and recall scores showing high proportion of correct calls, and a high proportion of correct positive calls. The Easy Ensemble model does NOT have a high precision score for the High-Risk data, but has a high recall score, which indicates that the model has no False Negatives with the high risk set, which is desireable in this type of model. 

I believe the Geometric Mean is a combination of specificity and sensitivity, meaning it summarizes both how well the positive and negative classes were predicted. In that case, the Easy Ensemble Classifier has a slight edge as the better model.

See [Machine Learning Mastery](https://machinelearningmastery.com/tour-of-evaluation-metrics-for-imbalanced-classification/) for the explanation used of Geometric Mean.

## III. Questions Answered
### Resampling
>Which model had the best balanced accuracy score?
> 
> *The Native Random Oversampling model had the best accuracy score at .6612. The SMOTE model had the second highest accuracy score, which makes sense considering the modeling has balanced datasets.*
>
> Which model had the best recall score?
>
>*The Native Random Oversampling model also had the highest recall score .67 for High-Risk and .66 for Low-Risk*
>
> Which model had the best geometric mean score?
>
>*The Native Random Oversampling model also had the highest geometric mean score at .66*

### Ensemble Learning
> Which model had the best balanced accuracy score?
> 
> *The Easy Ensemble Classifier had the highest accuracy score at .9330*
>
> Which model had the best recall score?
> 
>*The Balanced Random Forest model has the highest recall score for the low-risk set of loan data with a recall of 1.00, meaning there were no False Negatives*
>
> Which model had the best geometric mean score?
>
>*The Easy Ensemble Classifier Model had the best geometric mean score at .93*
>
> What are the top three features?
>
>*The top 3 features (from highest to lowest) are total received interest, last payment amount, and total received principal.*
