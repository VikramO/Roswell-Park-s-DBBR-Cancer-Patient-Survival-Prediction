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

#### Data-Management
Data from 17 different tables were merged together with a common unique identifier field to create a master copy of the data.
Further, categorical data was numerically encoded using sklearn and missing values were imputed using the modes of the individual data fields. Summary statistics for each field were also computed.

#### Study-Design

*ADD HISTOGRAMS*

#### Exploratory-Data-Analysis

*CONDUCT LINEAR REGRESSIONS*

#### Validation-Strategies 
The performance of the XGBoost algorithm was evaluated by using an independent testing dataset to assess overall accuracy. Also, an ROC curve was constructed to assess the true positive and false positive rates of the model. The training/testing split used was 80%/20%


#### Model-Training_and_Tuning
Hyperparameters were selected by testing multiple models and selecting the set of hyperparameters that optimized model performance.

#### Results_Model-Performance_and_Interpretability
![image](https://user-images.githubusercontent.com/42708529/104829275-3e38e780-5840-11eb-874b-37a78d505ae0.png)
Figure A: table of various performance metrics 

Our model acheived an overall accuracy of 75%


![image](https://user-images.githubusercontent.com/42708529/104794191-04021400-5774-11eb-92f0-ba1e87fab068.png)
Figure B: ROC curve

The dotted orange line represents a theoretical model that predicts completely at random, i.e. a model with no actual predictive value. The blue line represents our model's performance on the test data. The further it stretches towards the top left corner, the better predictive value it has. Therefore, the area under the ROC curve can be thought of as a measure of the usefulness of the model. Our model achieved an area under the ROC curve of 70.84%
#### Solution-Video

