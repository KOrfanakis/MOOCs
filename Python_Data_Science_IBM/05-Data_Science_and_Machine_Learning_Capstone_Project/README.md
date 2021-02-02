# Data Science and Machine Learning Capstone Project - NYC 311 Complaint Dataset

<p align="center">
  <img width="500" src="https://images.unsplash.com/photo-1496588152823-86ff7695e68f?ixlib=rb-1.2.1&ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&auto=format&fit=crop&w=1350&q=80">
</p>
<p align="center"><em>Photo by Luca Bravo (Unsplash)</em></p>

This folder contains the notebooks I used to complete IBM's online course '[Data Science and Machine Learning Capstone Project](https://www.edx.org/course/data-science-and-machine-learning-capstone-project)' on edX. I completed the course in July 2020.

The course is organised into four modules, one for each of the problem set's four questions. I decided to follow the same structure and present the answer to each question in a separate notebook. There is an additional notebook (titled 'Quiz on Data Ingestion') whose purpose is to familiarise the reader with the datasets. 

At the end of each module, a quiz section is used for assessment. I have also included this section at the end of each notebook. 

I have also organised the same analysis as one [Kaggle notebook](https://www.kaggle.com/korfanakis/capstone-project-nyc-311-complaint-dataset). 

<br>

---

**Table of Contents**

1. [Problem Statement](Problem-Statement)
2. [Datasets](Datasets)
3. [Approach](Approach)
4. [Results](Results)
5. [Resources Used](Resources-Used)

---

<br>

## Problem Statement

New York City residents use the 311 system to report complaints about non-emergency problems to local authorities. Various agencies in New York are assigned these problems. The Department of Housing Preservation and Development of New York City is the agency that processes 311 complaints that are related to housing and buildings.

In the last few years, the number of 311 complaints coming to the Department of Housing Preservation and Development has increased significantly. Although these complaints are not necessarily urgent, the large volume of complaints and the sudden increase impact the agency's overall efficiency.

Therefore, the Department of Housing Preservation and Development has approached your organisation to help them manage the large volume of 311 complaints they are receiving every year.

The agency needs answers to several questions. Data and analytics must support the answers to those questions. These are their  questions:

- Which type of complaint should the Department of Housing Preservation and Development of New York City focus on first?
- Should the Department of Housing Preservation and Development of New York City focus on any particular set of boroughs, ZIP codes, or street (where the complaints are severe) for the specific type of complaints you identified in response to Question 1?
- Does the Complaint Type you identified in response to question 1 have an apparent relationship with any particular characteristic or characteristics of the houses or buildings?
- Can a predictive model be built for a future prediction of the possibility of complaints of the type you have identified in response to question 1?

Your organisation has assigned you as the lead data scientist to provide the answers to these questions. You need to work on getting answers to them in this Capstone Project by following the standard approach of data science and machine learning.

<br>

## Datasets

We will use two datasets from the Department of Housing Preservation and Development of New York City to address their problems. The datasets are not included in this repository. You can have a look at the [Quiz on Data Ingestion](https://github.com/KOrfanakis/MOOCs/blob/main/Python_Data_Science_IBM/05-Data_Science_and_Machine_Learning_Capstone_Project/Quiz_on_Data_Ingestion.ipynb) notebook for a quick overview of the datasets.

### 311 Complaint Dataset

This dataset is available at the [NYC OpenData website](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9). For our convenience, the course authors have already downloaded the data and placed it on an [IBM server](https://cocl.us/311_NYC_Dataset). The downloaded data will have complaints submitted between 2010 and 2020. We should download data only for relevant columns so that the data volume is manageable.

### PLUTO Dataset for Housing

We can download the PLUTO dataset as a zip file from [this link](https://data.cityofnewyork.us/City-Government/Primary-Land-Use-Tax-Lot-Output-PLUTO-/xuk2-nczf ). After extracting the file, we should have five CSV files for the five New York City boroughs: Bronx, Brooklyn, Manhattan, Queens, and Staten Island.

<br>

## Approach

We can answer the first two problem statements by performing Exploratory Data Analysis (EDA) on the 311 Complaint Dataset. We essentially need two tools: Pandas, for extracting useful information from our dataset, and Matplotlib for visualising the results.

For the third problem, we need to include building characteristics in our analysis. Therefore, we will first merge the two datasets and then examine the correlation between the most common complaint type and the building characteristics.

Finally, the fourth problem statement requires the basic Machine Learning (ML) workflow. After preprocessing the merged dataset, we will build two ML models for predicting a building's chance of showing the most common complaint type. The algorithms used are Random Forest and XGBoost classifier.

<br>

## Results

In summary, my findings are the following:

- **Question 1**: 'HEAT/HOT WATER' is the most frequent complaint type.
- **Question 2**: The Bronx is the most affected borough by this complaint type. The ZIP code with the highest number of complaints about 'HEAT/HOT WATER' is 11226 and belongs in Brooklyn. Finally,  Grand Concourse is the most affected street in New York City and belongs in the Bronx.
- **Question 3**: Correlation analysis shows a  (moderate positive) correlation between the total number of 'HEAT/HOT WATER' complaints and several building characteristics/features. It is not surprising that these features are related to spatial dimensions (larger area leads to a higher possibility for a heating-related complaint).
- **Question 4**: We could build two predictive models for future prediction of the possibility of getting a 'HEAT/HOT WATER' complaint in the Bronx. The XGB classifier (accuracy ~ 82%) performs better than the Random Forest classifier (accuracy ~ 76%).

<br>

## Resources Used

Python Version: 3.7 <br>
Jupyter Notebook Version: 5.7.8<br>
Packages: pandas, sklearn, numpy, matplotlib, seaborn, imblearn, xgboost, geopandas, scipy.

