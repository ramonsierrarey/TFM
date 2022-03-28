# TFM - Análisis de expansión de negocio

Pasos:
1. Crear base de datos con los nombres de los centros comerciales existentes en la península. Lo conseguimos escrapeando la web: https://www.centro-comercial.org
   Output: Generamos un excel con los nombres de los centros comerciales y la dirección web para extraer información de la web. 
   Al no contener información correcta en algunos campos, optamos por pasar el output generado por la API de Google para conseguir información de la dirección.
2. Creamos base de datos con el listado de centros comerciales y obtenemos de la API de Google: Latitud, Longitus, Dirección y Código postal.
   Input: fichero "Centros_Comerciales.xlsx"
   Output: fichero "XXXXXXXXXX.xlsx"
   
![alt text](https://github.com/[ramonsierrarey]/[TFM]/blob/[jpg]/Spain_map_CC.jpg?raw=true)

3. Necesitamos ubicar, con su Latitud y Longitud, los códigos postales del pais, 
   Input: Fuente externa: Base datos códigos postales "XXXXXXXXXXXXXXXXXXXX.xlsx"
   Output: 
