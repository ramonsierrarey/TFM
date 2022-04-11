# TFM - Análisis de expansión de negocio

Pasos:

0. Necesitamos ubicar, con su Latitud y Longitud, los códigos postales del pais, 
   Input: Fuente externa: Base datos códigos postales "Datos_CP.xlsx". Donde obtendremos listado de códigos postales de España y su tamaño de mercado (€).
   Output: "Codigos Postales.csv".

  <div align="left"><img src="https://user-images.githubusercontent.com/56726458/161086803-b24acbf4-8cc3-4bc6-9991-82bcbddbff45.JPG" width="286" height="233"> 

1. Crear base de datos con los nombres de los centros comerciales existentes en la península. Lo conseguimos escrapeando la web: https://www.centro-comercial.org
   Output: Generamos un excel con los nombres de los centros comerciales y la dirección web para extraer información de la web. 
   Al no contener información correcta en algunos campos, optamos por pasar el output generado por la API de Google para conseguir información de la dirección.
2. Creamos base de datos con el listado de centros comerciales. Lo conseguimos escrapeando la web: https://www.centro-comercial.org
   Para determinar su ubicación. Lo conseguimos mediante la API de Google Maps, obteniendo: Latitud, Longitus, Dirección. De la Dirección extraeremos el código postal.
   Input: https://www.centro-comercial.org
   Output: fichero "Centros_Comerciales.csv"
   
<div align="left"><img src="https://user-images.githubusercontent.com/56726458/160465542-9ff20102-2ded-491a-b6fc-c69b39414301.JPG" width="286" height="233">
   
