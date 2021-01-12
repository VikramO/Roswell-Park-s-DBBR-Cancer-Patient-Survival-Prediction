# Team-4-AIM-Datathon
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
* [Exploratory Data Analysis](#Study-Design)
* [Validation Strategies (Train and Test Data Pre-processing, Training/Validation Split)](#Validation-Strategies)
* [Model Training,Tuning (XGBoost with AUC performance metric)](#Model-Training_and_Tuning)
* [Results,Model Performance,Interpretability](#Results_Model-Performance_and_Interpretability)
* [Solution Video](#Solution-Video)
  * Link a short video (unlisted Youtube link) that walks through your approach from github and code from google collab.
* [Acknowledgments](#acknowledgments)

#### Problem
- Physcians are overwhlemed with patient cancer data, and would benefit from a system that outlined indiviaulized patients risk factors based  patient's background like gender, date of birth, enthicity aswell as familial history, primiary site, cancer stage and grading to augment their clinical decision making. 

#### Solution
- A clinical decision system to help physicians keep track of their patients' progress using their background and individualized molecular level data. A second solution was also developed to help physicians keep track of the stage progression of their patients' cancer types. The notebook for this solution deals with prostate cancer.

*Note*: The ML pipeline was the same for both solutions, therefore notes in the patient survival notebook can be used for the stage progression notebook.

#### ML-Pipeline
--UPDATE THIS--

- ML WorkFlow depicting the solution below.![Image](https://github.com/aimsymposium/Project-sample/raw/main/MLpipeline.png)
- Add a link to your code(Google Colab). Refer to this [sample notebook](https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing) for further details.
#### Data-Management
Refer to Data Pre-Processing subtitle in the [Google Collab notebook](https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing) for more detail. 
- Data Pre-processing/ Cleansing/Transformations(Changing column names, Merging different data sources, etc). 
- Imputing missing data using mode of the feature
#### Exploratory-Data-Analysis
(2000 patients with various cancer types were included. A diverse patient population race was involved including whites (1860 [93%]),  African Americans (88 [4.5%]), American Indians (12 [0.6%]), Asians (7 [0.35%]),  Alaskan Natives (12 [1%]), Native Hawaiians (2 [0.15%]), and from other races (7 [0.45%]). The median age (interquartile range) was 62 (54-70) years old.  
36% of the patients had a paternal history with cancer and the greatest proportion was 10% prostate cancer. 39% of the patients had a maternal history with cancer and the greatest proportion was 11% breast cancer. 
Out of 785 males,the majority of the tumors were from the prostate gland as the primary site (371[47.2%]),adenocarcinoma(496 [63%]), grade III: Poorly differentiated , dedifferentiated (369 [47%]), and stage 1 (478[60%]) . 
Out of 1215 females, the majority of the tumors were from the breast upper outer quadrant primary site(300 [24.69%]), infiltrating duct carcinoma(535 [44%]), grade II: moderately differentiated, intermediate differentiated (522 [43%]), and stage 1 (737 [60%]).

#### Validation-Strategies 
Refer to Train and Test Data Pre-processing, Training/Validation Split subtitles in the [Google Collab notebook](https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing) for more detail. 

-Train and Test Data Pre-processing
-Training/Validation Split

#### Model-Training_and_Tuning
Refer to XGBoost subtitles in the [Google Collab notebook](https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing) for more detail. 

#### Results_Model-Performance_and_Interpretability
Refer to Results,.... subtitles in the [Google Collab notebook](https://colab.research.google.com/drive/1q05LU9_PN0izalQToJjcnErrsL3kc4Ji?usp=sharing) for more detail. 

-Include Summary of Results/Discussion and Picture of Results here.

-XGBoost

![Image](https://github.com/aimsymposium/Project-sample/blob/main/XGBoost.PNG)

#### Solution-Video
--UPDATE THIS--

[![Watch the video](https://github.com/Code-and-Response/Liquid-Prep/blob/master/images/IBM-interview-video-image.png)](https://youtu.be/vOgCOoy_Bx0)


#### Acknowledgments
