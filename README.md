# Business Expansion Analysis
![Logo_TFM](https://user-images.githubusercontent.com/56726458/173163556-e6e82cca-f374-400a-8a60-4f13fa8ca043.JPG)
  
  This project has been developed by [Francisco Javier Planells](https://github.com/fplanells) and [Ramon Sierra Rey](https://github.com/ramonsierrarey)  
Master Final Project - Master in Data Science - [KSchool](https://www.kschool.com/) Madrid.  
To get more detail information visit [Memoria](https://github.com/ramonsierrarey/TFM/wiki/Memoria) in wiki section.
  
  # Table of Contents

[Introduction](#introduction) <br>
[Methodology](#methodology) <br>
[Data acquisition](#Data-acquisition) <br>
[Data cleansing and preparation](#Data-cleansing-and-preparation) <br>
[Analysis](#analysis) <br>
[Frontend](#frontend) <br>
[Requirements](#requirements) <br>
[Modeling and Measures](#modeling-and-measures) <br>
[Conclusions](#conclusions) <br>


# Introduction

  Our idea began when we would like to know in an expansion perspective... If we would like to open a new **homefurnishing** selling point, where can we open it? There´s a lot of posibilities. With a low invenstment we can open in a rent space (in any shoping center area). If we know the behabour of our customers, the market size of the product that we are selling... Could we detect the potencial point to open?  
  
  With our "Business Expansion Analysis", we would like to answer these questions and  we try to create a support business tool to help in the decision process when you think to open a small shop in a spanish shoping center.

  
# Methodology

We have used linear regression and non-linear regression models such as Decision Trees or K-Nearest Neighbours to detect the best machine learning techniques.


  
# Data acquisition
We get two types of sources to begin the process: external and internal data:
* _external data_:We receive the data. There are two files: "Datos_CP.xlsx" (all spanish zip code and size of the homefurnishing market) and "Sales_per_point.csv"  (an theorical exercise of differente shops and sales per zip code).

* _internal data_: we generate the data.Method used: Web Scraping. We have used **Beautifulsoup4** library to scrape and create a data base.  
                      - First step. Get the name of the shoping centers in Spain, from www.centro-comercial.org.  
                      - Second step. Get the address and extract the Zip Code of the shopping centres names with **Google API** (Geocoding API).  
                      - Third step. Get the latitude and longitude of all the spanish zip codes ("Datos_CP.xlsx") with **Google API**.

# Data cleansing and preparation
We have the sales of our current shoping center stores. We link sales per zipcode and sales point with their coordinates (lat and lon) and with this we get the sales per distance and the size of the market. Doing this, we've detected that the influence area of this kind of business is about 20 km. With this information, we have calculated the distance between all spanish zipcodes, geting a file with the areas per zip code of 20 km.  


# Analysis
We would like to predict the sales of a new homefurnishing shop (in a shopping centre). We base this analysis taking in cosideration the market share  that cover a zip code and the distance between zip codes. 

  
# Frontend
we use **Power BI Desktop** as a frontend tool. Power BI desktop version is required to be installed and dive into the report (PBI_Visualization.pbi).
But loging account is not needed.


# Requirements

We'll use the Anaconda virtual environment with Python 3.7.
Conda version used==4.13.0

**CODE**
````markdown
conda create -n TFM python=3.7
conda active TFM
conda install pandas openpyxl matplotlib jupyter
````
All the dependencies packages has been installed.

### Anaconda Python Packages

* pandas
* googlemaps (pip install included in notebook)
* matplotlib
* jupyter
* scikit-learn (pip install included in notebook with specific version)

For avoiding future compatibility issues, here are the versions of the main key libraries used:

```
pandas==1.3.5
googlemaps==4.6.0
matplotlib==3.5.1
jupyter==1.0.0
scikit-learn==1.0.2
```
An conda export ennvironment file (.yml extension) has been created. It is uploaded in the repository as *TFM_environment.yml*.

# Modeling and Measures

We have used several ML Classifiers algorithms, mostly from `scikit-learn`:

* Linear Regression

![LR_Model](https://user-images.githubusercontent.com/56726458/173640185-e1c3fe5a-e983-4787-9e3c-6279a6e3e17e.JPG)

* K-nearest Neighbors + GS (GridSearch)

![K-Neighbors_Model](https://user-images.githubusercontent.com/56726458/173641015-00e006f4-01a0-4d08-91ed-441e8a7a8062.JPG)

* Decision Tree + GS

![DT_Model](https://user-images.githubusercontent.com/56726458/173644907-4cfe1ea2-1569-4c73-bcb0-d32162aa426c.JPG)

All these models with differente analysis metrics:

* MAE. Mean Absolute Error. (Mean of all the prediction errors)  
* MAPE. Mean Absolute Percentage error. (Mean Absolute Error / Mean real values)  
* RMSE. Root Mean Square Error (High errors affects more than small ones)  
* Correlation (between the prediction and the real value)  
* Bias (Average of errors)  

![Compare_metrics](https://user-images.githubusercontent.com/56726458/173650957-1c355721-6f4b-4e17-889f-815c5fcdcaeb.JPG)  


We analize all the models, metrics and we select Decision Tree model to get our market share prediction (MShare_prediction) and calculate the potential sales.  


![06_Output](https://user-images.githubusercontent.com/56726458/173892537-3c41416c-0484-4941-89e8-3404647e7a7e.JPG)  



# Conclusions  


At the end of all this Master's Thesis, this exercise helps us to apply and practice with diferent techniques and methodology learnt. It learns us to obtain, manage, analice and predict data. Sometimes the data was difficult to get, or we had to find the way to build it. It has been a good exercise.

The general overview about what we would like to find was clear. From data science perspective we would like to resolve or give more information in the moment of invest in a new shop or a new business format. We think it has been resolved. There has been limitations to get data base of some varibles (we got it from external sources or it was modified from original data), but we are conscious that with these new skills learned and our business knowledge, We have been able to face them.

In this project we have developed a base way to get potential locations. The model can be more complex, there are more varibles to take in consideration like purchase power, rent space,..., but the concept and the general idea is the same.

There is more specific information at wiki
