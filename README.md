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
   
This project has been developed by [Francisco Javier Planells](https://github.com/fplanells) and [Ramon Sierra Rey](https://github.com/ramonsierrarey)
  Master Final Project - Master in Data Science - [KSchool](https://www.kschool.com/) Madrid.
  
  # Table of Contents

[Introduction](#introduction) <br>
[Methodology](#methodology) <br>


# Introduction

  Our idea began when we would like to know in an expansion perspective... If we would like to open a new selling point, where can we open it? There´s a lot of posibilities. With a low invenstment we can open in a rent space (in any shoping center area). If we know the behabour of our custmoers, the market size of the product that we are selling, Could we detect the potencial point to open?

  
# Methodology
  
  ## Data adquisition
* We get two types of external sources to begin the process: esternal and internal data.
* _external data_: two files: "Datos_CP.xlsx" and "Sales_per_point.csv"
* _internal data_: Web Scraping. We used **Selenium Webdriver** to scrape and create a data base with the name of the shoping centers in Spain, from www.centro-comercial.org and **Google API** (Geocoding API) to get the address and extract the Zip Code.
  **Google API**. We used to get the latitude and longitude of spanish zip code (file "Datos_CP.xlsx").

## Data cleansing and preparation


## Analysis

  
## Frontend
* we use a frontend from micorosft: Power BI Desktop. We show ... 

