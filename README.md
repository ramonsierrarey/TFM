# TFM - Análisis de expansión de negocio

Pasos:
1. Crear base de datos con los nombres de los centros comerciales existentes en la península. Lo conseguimos escrapeando la web: https://www.centro-comercial.org
   Output: Generamos un excel con los nombres de los centros comerciales y la dirección web para extraer información de la web. 
   Al no contener información correcta en algunos campos, optamos por pasar el output generado por la API de Google para conseguir información de la dirección.
2. Creamos base de datos con el listado de centros comerciales y obtenemos de la API de Google: Latitud, Longitus, Dirección y Código postal.
   Input: fichero "Centros_Comerciales.xlsx"
   Output: fichero "XXXXXXXXXX.xlsx"
   
<div align="center"><img src="https://user-images.githubusercontent.com/56726458/160465542-9ff20102-2ded-491a-b6fc-c69b39414301.JPG" width="286" height="233">

3. Necesitamos ubicar, con su Latitud y Longitud, los códigos postales del pais, 
   Input: Fuente externa: Base datos códigos postales "XXXXXXXXXXXXXXXXXXXX.xlsx"
   Output: 
   
  <div align="center"><img src="https://user-images.githubusercontent.com/56726458/161086803-b24acbf4-8cc3-4bc6-9991-82bcbddbff45.JPG" width="286" height="233"> 
