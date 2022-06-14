# Business Expansion Analysis
![Logo_TFM](https://user-images.githubusercontent.com/56726458/173163556-e6e82cca-f374-400a-8a60-4f13fa8ca043.JPG)
  
  This project has been developed by [Francisco Javier Planells](https://github.com/fplanells) and [Ramon Sierra Rey](https://github.com/ramonsierrarey)  
Master Final Project - Master in Data Science - [KSchool](https://www.kschool.com/) Madrid.
  
  # Table of Contents

[Introduction](#introduction) <br>
[Methodology](#methodology) <br>
[Requirements](#requirements) <br>
[Conclusions](#conclusions) <br>


# Introduction

  Our idea began when we would like to know in an expansion perspective... If we would like to open a new **homefurnishing** selling point, where can we open it? There´s a lot of posibilities. With a low invenstment we can open in a rent space (in any shoping center area). If we know the behabour of our customers, the market size of the product that we are selling... Could we detect the potencial point to open?  
  
  With our "Business Expansion Analysis", we would like to answer these questions and  we try to create a support business tool to help in the decision process when you think to open a small shop in a spanish shoping center.

  
# Methodology
  
  ## Data adquisition
We get two types of sources to begin the process: esternal and internal data:
* _external data_:We receive the data. There are two files: "Datos_CP.xlsx" (all spanish zip code and size of the homefurnishing market) and "Sales_per_point.csv"  (an theorical exercise of differente shops and sales per zip code).

* _internal data_: we generate the data.Method used: Web Scraping. We have used **Beautifulsoup4** library to scrape and create a data base.  
                      - First step. Get the name of the shoping centers in Spain, from www.centro-comercial.org.  
                      - Second step. Get the address and extract the Zip Code of the shopping centres names with **Google API** (Geocoding API).  
                      - Third step. Get the latitude and longitude of all the spanish zip codes ("Datos_CP.xlsx") with **Google API**.

## Data cleansing and preparation
We detect that the influence area of this kind of business is about 20 km. We calculate distance betwwen zipcodes to get areas per zip code of 20 km.  
we have the sales of our current shoping center stores. We link sales per zipcode and sales point  with their coordinates (lat and lon). We get the sales per distance and the size of the market.

## Analysis
We would like to predict the sales of a homefurnishing shop (in a shopping centre). we base this analysis taking in cosideration the market share  that cover a zip code and the distance between zip codes. 

  
## Frontend
we use **Power BI Desktop** as a frontend tool. Power BI desktop version is required be installed to dive into the report ( PBI_Visualization.pbi).
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

# Conclusions



# TFM - Análisis de expansión de negocio

Pasos:

0. Necesitamos ubicar, con su Latitud y Longitud, los códigos postales del pais, 
   * Input: Fuente externa: Base datos códigos postales "Datos_CP.xlsx".
   * Output: "Codigos Postales.csv". Donde obtendremos listado de códigos postales de España "CP", su tamaño de mercado (€) y ubicación.

  <div align="left"><img src="https://user-images.githubusercontent.com/56726458/161086803-b24acbf4-8cc3-4bc6-9991-82bcbddbff45.JPG" width="286" height="233"> 

1. Creamos base de datos con el listado de centros comerciales. Lo conseguimos escrapeando la web: https://www.centro-comercial.org
   Para determinar su ubicación. Lo conseguimos mediante la API de Google Maps, obteniendo: Latitud, Longitus, Dirección. De la Dirección extraeremos el código postal.
   * Input: https://www.centro-comercial.org
   * Output: fichero "Centros_Comerciales.csv"
   
<div align="left"><img src="https://user-images.githubusercontent.com/56726458/160465542-9ff20102-2ded-491a-b6fc-c69b39414301.JPG" width="286" height="233">

