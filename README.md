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
* [Exploratory Data Analysis](#Exploratory-Data-Analysis)
* [Validation Strategies (Train and Test Data Pre-processing, Training/Validation Split)](#Validation-Strategies)
* [Model Training,Tuning (XGBoost with AUC performance metric)](#Model-Training_and_Tuning)
* [Results,Model Performance,Interpretability](#Results_Model-Performance_and_Interpretability)
* [Solution Video](#Solution-Video)
  * Link a short video (unlisted Youtube link) that walks through your approach from github and code from google collab.
* [Acknowledgments](#acknowledgments)

#### Problem

There are many factors that impact cancer patient survival. These include factors such as  gender, date of birth, enthicity as well as familial history, primiary site, cancer stage and grading among others. Our goal is to aid physicians in their decision making process by developing a machine learning model to assess the likelihood of survival based on these factors.



#### Solution
- A clinical model based on the industry standard XGBoost algorithm was created to help physicians assess patients' risk by incorporating the data from Roswell Park. 

#### ML-Pipeline


![image](https://user-images.githubusercontent.com/42708529/104794121-a5d53100-5773-11eb-8bb9-e901b48b661e.png)
https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing(https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing) for further details.


#### Data-Management
Data from 17 different tables were merged together with a common unique identifier field to create a mastr copy of the data.
Further, categorical data was numerically encoded using sklearn and missing values were imputed using the mode of the individual data field. Summary statistics for each field were computed.
#### Exploratory-Data-Analysis
(2000 patients with various cancer types were included. A diverse patient population race was involved including whites (1860 [93%]),  African Americans (88 [4.5%]), American Indians (12 [0.6%]), Asians (7 [0.35%]),  Alaskan Natives (12 [1%]), Native Hawaiians (2 [0.15%]), and from other races (7 [0.45%]). The median age (interquartile range) was 62 (54-70) years old.  
36% of the patients had a paternal history with cancer and the greatest proportion was 10% prostate cancer. 39% of the patients had a maternal history with cancer and the greatest proportion was 11% breast cancer. 
Out of 785 males,the majority of the tumors were from the prostate gland as the primary site (371[47.2%]),adenocarcinoma(496 [63%]), grade III: Poorly differentiated , dedifferentiated (369 [47%]), and stage 1 (478[60%]) . 
Out of 1215 females, the majority of the tumors were from the breast upper outer quadrant primary site(300 [24.69%]), infiltrating duct carcinoma(535 [44%]), grade II: moderately differentiated, intermediate differentiated (522 [43%]), and stage 1 (737 [60%]).

#### Validation-Strategies 
The performance of the XGBoost algorithm was evaluated by using both an independent testing dataset and through the construction of an ROC curve to assess the true positive and false positive rate of the model.

-Train/Test Split: 80/20 



#### Model-Training_and_Tuning
Hyperparameters were selected by testing multiple models and selecting the set of hyperparameters that optimized model performance.

#### Results_Model-Performance_and_Interpretability
![image](https://user-images.githubusercontent.com/42708529/104829275-3e38e780-5840-11eb-874b-37a78d505ae0.png)
Figure A table of various performance metrics 

Our model acheived an overall accuracy of 75%


![image](https://user-images.githubusercontent.com/42708529/104794191-04021400-5774-11eb-92f0-ba1e87fab068.png)
Figure B ROC curve

The dotted orange line represents a theoretical model that predicts completely at random, i.e. a model with no actual predictive value. The blue line represents our model's performance on the test data. The further it stretches towards the top left corner, the better predictive value it has. Therefore, the area under the ROC curve can be thought of as a measure of the usefulness of the model. Our model achieved an area under the ROC curve of 70.84%
#### Solution-Video
--UPDATE THIS--

[![Watch the video](https://github.com/Code-and-Response/Liquid-Prep/blob/master/images/IBM-interview-video-image.png)](https://youtu.be/vOgCOoy_Bx0)


#### Acknowledgments
