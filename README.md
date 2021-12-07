# Answers to Five of Your Burning Questions About Heart Failure! 
### **A Dataset Analysis**

Alternate title: We Analyzed An UNBELIEVABLE Heart Failure Prediction Dataset and Here's What We Found: (Answers to 5 Heart Failure Questions That Will CHANGE YOUR LIFE)

## Authors:
Chioma Okechukwu - Chi-O 

Krishna Patel - kptg0

William Dolan - Will-Dolan-VI

## Introduction:
This is our analysis of a dataset about patients that suffered from heart failure.

The dataset, which can be found [here](https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/) and on Kaggle [here](https://www.kaggle.com/fedesoriano/heart-failure-prediction), is a combination of several datasets from America, Hungary, Switzerland and Germany and has a total of 918 records. The records include patient data such as sex, blood pressure and cholesterol for example, as well as whether the patient suffered from any heart disease.

In our analysis, we use the information in the dataset to try to answer questions about the frequency and effects of heart disease. We also look into the frequency and relationships of different causes of chest pain. 
We chose these questions in particular because they may represent causes of or ways to identify heart disease. Answers to these questions may help identify people with, or at risk of getting heart disease.

## Discussion:


![alt text](./charts/cholVsDisease.PNG?raw=true)

## Conclusion:
Overall, we felt like this analysis turned out well as we managed to find information and draw conclusions from it.   Some things we reflected on were:
- Graphs that we chose showed alot of information
- 


However, we had some things we could improve on:
- Choose an improved dataset that does not contain errors or N/A's
- 

## Acknowledgements:

We thank Fedesoriano for putting this data set together.

This project was submitted as the final course project for CSCI 2000U during Fall 2021. The authors ensure that the work done is original and resources are rightfully credited. 



## README:
##### Installation
Use the package manager pip to install plotly.
```
pip install plotly==5.4.0
```

##### Importing:

Use these commands to import the following libraries:
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib
import matplotlib.pyplot as plt

import plotly.express as px
from plotly.subplots import make_subplots
import plotly.graph_objects as go
```

##### Loading Dataset:

To load the data set use the following code:
```
df = pd.read_csv('heart.csv')
```
