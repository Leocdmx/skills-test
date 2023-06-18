# skills-test
Esta prueba está destinada a evaluar el nivel en capacidades técnicas de análisis de datos y, sobre todo, capacidad de resolución de problemas. Existen muchas formas de resolver los problemas que se plantean, se pide hacerlo apoyandose en cualquier recurso a disposición del evaluado estando permitido usar cualquier tecnología o documentación a su alcance.

La prueba se basa en dos partes, una primera parte enfocada a la minería y transformación de datos y una segunda parte orientada a su análisis.

## Primera parte
Para esta primera parte será necesario hacer uso del API Nominatim [https://geopy.readthedocs.io/en/stable/] y del API Open Charge Map [https://openchargemap.org/site/develop/api#/]. El objetivo es partir de la base de datos auto_coloca_2022_v2_clean.xlsx (en la carpeta compartida de la prueba) y realizar los siguientes procesos:
* Utilizar el API Nominatim para, a partir del campo "town_name_cte" obtener las coordenadas espaciales de cada uno de los records de la base de datos (para los que esté disponible)
* Utilizar el API openchargemap para obtener el listado geolocalizado de todas las estaciones de carga eléctricas en México
* Utilizar el shapefile de municipios mexicanos (en la carpeta compartida: inegi_refmunicip_2010.shp) para obtener el número de estaciones de carga en el municipio de cada uno de los records de la base de datos y unir dicho número en una columna a la base de datos.

## Segunda parte
Partiendo de la base de datos ampliada en la primera parte con el número de estaciones de carga existentes en el municipio se pide:
* Hacer un descriptivo de las variables de la base de datos (seleccionar un par de variables, no es necesario que sean todas)
* Testear la hipótesis de que cuantas más estaciones de carga haya en el municipio de un cliente más probable es que este pida un crédito verde (variable "credito_verde" en la base de datos).
* Entrenar un clasificador supervisado (da igual el algoritmo) para la variable "credito_verde". Se pueden usar tantas variables como se quiera de la base de datos.

## Entrega de los resultados
Los resultados se entregarán realizando una Pull Request en este repositorio.
Todos los datos necesarios para llevar a cabo las tareas descritas están en la carpeta compartida de la prueba.
En casso de no poder completar las tareas de la primera parte, en la carpeta compartida se podrá encontrar el archivo "upgradeddb.xlsx" con los datos necesarios para poder llevar a cabo la segunda parte.
A mayores de los puntos descritos anteriormente se valorará lo siguiente:
* Uso del mayor número de tecnologías posible.
* Escribir código limpio siguiendo las buenas prácticas.
* Redactar explicaciones donde sea necesario.
* Un uso correcto del control de versiones.