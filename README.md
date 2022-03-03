# Projects

Welcome to my projects overview with short descriptions of every project.
At the end of this file you find the technical requirements.

---

# __Project 1: EDA Project__

## __King County Real Estate__

This notebook is about my first EDA project during the Data Science bootcamp at neue fische. 
The task of the project was to recommend suitable properties for a pre-selected client. The data set included information on the number of rooms and bathrooms, year of construction, size of the house and property, and budget. Each of the bootcamp participants could choose one customer before starting with the EDA, who was already presented with his/her budget and ideas a.o. regarding size, number of bathrooms and rooms. 

[Notebook](Project_1/notebooks): Jupyter Notebook

[Images](Project_1/images): Images, plots and maps.

[Dataset](Project_1/data): I used the King County House Sales dataset. Here, the focus is on EDA though it was required to demonstrate an entire Data Science Lifecycle using linear regression. The task will be to perform an extensive EDA and to train a explanatory linear regression model. The task is not only to explain the data but also to evaluate how well the model is fitting the data. 

[Stakeholder Presentation](https://github.com/IronMan2483/Projects/blob/main/Project_1/Stakeholder_JP.pdf): PDF file

---
---

# __Project 2: Machine Learning__

## __AirQo Ugandan Air Quality Forecast Challenge__

This notebook is about my second project during the Data Science bootcamp at neue fische. 

The task of the project was the prediction of the air quality in the Ugandan capital Kampala - e.g. relevant for local TV stations - and thus the early warning of harmful fine dust concentrations. The data set included weather and wind data as well as measurement data from the external provider AirQo.
The project included EDA and data visualization, a "small time series", the selection of different machine learning models and the presentation of results at the end of the project.

In contrast to the 1st project this was a group work with partly also pair programming and error analysis, as it also belongs to the normal working day of a Data Analyst and Data Scientist. The bootcamp participants could choose from given projects and get together in groups. 

[Notebook](https://github.com/IronMan2483/Projects/blob/main/Project_2/notebook/Air_quality_Uganda_final.ipynb): Jupyter Notebook

[Images](https://github.com/IronMan2483/Projects/tree/main/Project_2/images): Images, plots and maps.

[Dataset](https://zindi.africa/competitions/airqo-ugandan-air-quality-forecast-challenge/data): The dataset is from a challenge which was created on Zindi, the data science competition platform with the mission of building the data science ecosystem in Africa. The objective of this challenge is to accurately forecast air quality (as measured by PM2.5 µ/m3) for each hour of the coming 25 hours across five locations in Kampala Uganda. Forecasts will be based on the past 5 days of hourly air quality measurements at each site.
Zindi provided .csv files with train and test data but also meta data with location details. The meta data was excluded in the project.

[Stakeholder Presentation](https://github.com/IronMan2483/Projects/blob/main/Project_2/Project%202_%20ML-Uganda_Team%20RPK.pdf): PDF file

---
---

## __Technical preparation__


### __Requirements__

pyenv
python==3.9.4
Setup

For this purpose you use following commands:

````
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt

````
