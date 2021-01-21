# Team 4 : AIM-Datathon
## Project Title: Predicting patient survival and stage progression in cancer patients

Team Members: Vikram, Matthew, and Mira

Link to AIM Datathon: https://www.kaggle.com/c/aimdatathon2020/leaderboard <br>
Link to Google Collab Notebooks: 
Patient Survival: https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing
Stage Progression: https://colab.research.google.com/drive/1Un_WAmI-dcFe0WXgzBgwtBaNMMdDyJEv?usp=sharing

### Contents

* [Problem](#Problem)
* [Solution](#Solution) (Clinical Revelance of the Model)
* [ML Pipeline](#ML-Pipeline)
* [Data Management](#Data-Management)
* [Study Design](#Study-Design)
* [Exploratory Data Analysis](#Exploratory-Data-Analysis)
* [Validation Strategies (Train and Test Data Pre-processing, Training/Validation Split)](#Validation-Strategies)
* [Model Training,Tuning (XGBoost with AUC performance metric)](#Model-Training_and_Tuning)
* [Results,Model Performance,Interpretability](#Results_Model-Performance_and_Interpretability)
* [Solution Video](#Solution-Video)
* [Acknowledgments](#acknowledgments)

#### Problem

There are many factors that impact cancer patient survival. These include gender, date of birth, enthicity as well as familial history, primiary site, cancer stage and grading among others. Our goal is to aid physicians in their decision making process by developing a machine learning model to assess the likelihood of survival based on these factors.



#### Solution
- A clinical model based on the industry standard XGBoost algorithm was created to help physicians assess patients' risk by incorporating the data from Roswell Park Cancer Center. 

#### ML-Pipeline


![image](https://user-images.githubusercontent.com/42708529/104794121-a5d53100-5773-11eb-8bb9-e901b48b661e.png)
https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing(https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing) 

#### Data Management
Data from 17 different tables were merged together with a common unique identifier field to create a master copy of the data.
Further, categorical data was numerically encoded using sklearn and missing values were imputed using the modes of the individual data fields. Summary statistics for each field were also computed.

#### Data Pre-Processing
We process the data by encoding categorical columns and filling NaN values with the mode of the feature. Notice how we do not normalize the data or check for multicollinearity. This will make sense very shortly. We also notice that there is mild class imbalance between the two categories.

#### Study Design
![histogram](https://user-images.githubusercontent.com/42708529/105274599-7c4d4880-5b6b-11eb-9372-104513620c3c.png)
Figure A: Histogram of Cancer Types

![red_histogram](https://user-images.githubusercontent.com/42708529/105274646-9424cc80-5b6b-11eb-9c63-21c6e5dd861a.png)
Figure B: Histogram of Patient Ages


#### Validation Strategies 
The performance of the XGBoost algorithm was evaluated by using an independent testing dataset to assess overall accuracy. Also, an ROC curve was constructed to assess the true positive and false positive rates of the model. The training/testing split used was 80%/20%


#### Model Training, Tuning, and Validation
Hyperparameters were selected by testing multiple models and selecting the set of hyperparameters that optimized model performance.

#### Results: Model Performance and Interpretability
![image](https://user-images.githubusercontent.com/42708529/104829275-3e38e780-5840-11eb-874b-37a78d505ae0.png)
Figure C: table of various performance metrics 

Our model acheived an overall accuracy of 75%


![image](https://user-images.githubusercontent.com/42708529/104794191-04021400-5774-11eb-92f0-ba1e87fab068.png)
Figure D: ROC Curve for Survival Analysis

The dotted orange line represents a theoretical model that predicts completely at random, i.e. a model with no actual predictive value. The blue line represents our model's performance on the test data. The further it stretches towards the top left corner, the better predictive value it has. Therefore, the area under the ROC curve can be thought of as a measure of the usefulness of the model. Our model achieved an area under the ROC curve of 70.84%


#### Cancer Stage Progression Analysis
We applied the XGBoost model to the task of predicting tumor stage progression. For this task, we used the most prevalent cancer type in the dataset, which in this case happened to be prostate cancer. Here, the stsge of cancer is the target variable, and all of the other variables serve as predictors. The clinical relevance here is that when a physician is deciding whether to continue a certain course of treatment against a certain cancer, it is of critical importance to assess how quickly the tumor is progressing. Henceforth, this model serves as an additional tool to clinicians in their final assessment in the development of treatment plans.

#### Stage Progression Results

![results_stage_rogression](https://user-images.githubusercontent.com/42708529/105274874-1f05c700-5b6c-11eb-8903-37ae0a60e7b6.PNG)
Figure E: Table of Stage Progression Model Results
Our model acheived an overall accuracy of ~55%

![roc_stage_progression](https://user-images.githubusercontent.com/42708529/105274677-a69f0600-5b6b-11eb-9205-a5cbe82f134c.png)
Figure F: ROC Curve for Stage Progression
![decision_tree_2](https://user-images.githubusercontent.com/42708529/105274657-9ab34400-5b6b-11eb-8e9a-63a31c6e2277.png)
Figure G: Decision Tree for Stage Progression

#### Solution-Video





