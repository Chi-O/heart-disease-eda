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

### Initial look at the dataset:

Keeping in mind that all the records were people who suffered heart failure, we found that most of the patients were between the ages of 40 and 65, with the oldest being 77 and the youngest being 28. This suggests that in general, heart failure is much more common among older people, which isn't particularily surprising.

We didn't look into it much during the main analysis, but we also noticed that "oldpeak", a representation of the shape of the ST segment of an electrogram, was had more people with heart diseases with the higher values than people without. This is, again, an expected result. Higher values can indicate an "ST depression" which is a known effect of certain heart diseases.

We also noticed that Blood pressure and heart rate had weird spikes in the charts. We created a more detailed chart and found that the spikes were on multiples of 5 and 10, so we concluded that they occurred because some of the recorded data was rounded when it was input. The data comes from 5 different studies so it's possible that they had different conventions regarding how data was input.

![Blood Pressure Chart](./charts/bloodPressure.PNG?raw=true)

### Preprocessing:

Our first step in analyzing the data was to search for potential problems with the dataset. For the most part it was already very well formatted, though we had to remove 172 records with some missing data. Most of the removed datasets were due to cholesterol levels of 0 being recorded.

### Data Analysis:

Our first questions were whether age and cholesterol levels could cause or indicate heart disease and whether heart disease was more common among male or female patients. Unfortunately, the results for the former question ended up being fairly inconclusive. In the latter question however, our results show that heart disease was significantly more common among male patients than female patients. 

![Cholesterol Chart](./charts/sexVsDisease.PNG?raw=true)

Intregued by this, we investigated how other factors relate to heart disease.

The most interesting thing we found was probably the fact that the majority of patients with heart disease did not experience any significant chest pain (were asymptomatic - ASY). Our best guess for what could have caused this result was that the patients with heart disease either considered any chest pain "normal", or pains caused by heart disease weren't included when the data was collected.

![Chest Pain Chart](./charts/chestPainVsDisease.PNG?raw=true)

We also found that patients with heart disease had a lower heart rate on average. The difference between patients with heart disease and "healthy" patients is significant enough that, combined with other data, may prove to be a good indicator of heart disease.

![Heart Rate Chart](./charts/heartRateVsDisease.PNG?raw=true)

Predictably, patients with a flat or downwards ST slope also usually had heart disease while those with an upwards ST slope almost all had no heart disease. This result was expected because the shape of the ST slope on an electrogram is already known to be an indicator of heart disease.

Other than that, we found that patients with heart disease experienced excersise-induced much more than patients without and that more patients with heart disease had diabetic levels of blood sugar than patients without heart disease.

For the last two questions we farther investigated the types of chest pain.
Specifically:

-Typical Angina (TA)

-Atypical Angina (ATA)

-Non-Anginal Pain (NAP)

-Asymptomatic (ASY)

Our first question investigated whether there was a correlation between the chest pain types and age/sex. The results for this question ended up being inconclusive with all types of chest pains being fairly evenly distributed between sexes and across all ages.

For our final question, we searched for any correlation between the chest pains and cholesterol levels and it ended up being a bit more interesting. Patients that experienced Typical Angina, for the most part, had normal levels of cholesterol. Atypical Angina and Non-Anginal pains occurred among patients with all levels of cholesterol.  What's actually interesting though is the Asymptomatic column. We already saw that patients with heart disease were mostly "Asymptomatic", however, most patients with high cholesterol and experiencing chest pains have no heart disease. It's a rather lose correlation, but this does indicate high cholesterol but no chest pain could indicate heart disease. 

![Cholesterol and Chest Pain Chart](./charts/cholVsChestPain.PNG?raw=true)

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
<<<<<<< Updated upstream
##### Installation
=======

Installation
>>>>>>> Stashed changes
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
