# DESARROLLO DEL PROYECTO

 1.- AVANCE 1

a) Lee el archivo data_latinoamerica.csv con código Python en tu Visual Studio Code.  
Se importa pandas y se lee el archivo como pd.read_csv.
![Picture1](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture1.png)

 b) Comprueba que el dataset cargado tiene la cantidad de registros y columnas especificadas.
El dataset original tiene un total de 12,216,057 filas y 50 columnas.
![Picture2](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture2.png) 

c) Selecciona los países donde se expandirán: Colombia, Argentina, Chile, México, Perú y Brasil.
Se filtran los países tomando la variable “location key” como referencia ya que es la que esta normalizada.
![Picture3](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture3.png)

d)Filtra los datos en fechas mayores a 2021-01-01.
  Se filtran los datos con df_filtrado para obtener fechas mayores a 2021-01-01.
  

e) Compara a nivel de país para llenar valores faltantes.
Al filtrar los datos seleccionando la variable “location_key” quedan 7,692048 filas y 50 columnas.

  ![Picture4](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture4.png) 

f) Realiza una limpieza preliminar de los datos, eliminando registros nulos y corrigiendo los tipos de datos donde sea necesario, trata con valores medios, valores anteriores o valores siguientes.
Se eliminan valores nulos con el siguiente código. Quedando 3744 filas y 50 columnas.

![Picture5](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture5.png) 

g) Examina las características básicas del dataset para comprender la distribución de las variables clave como incidencia de COVID-19 e identifica las variables que consideras que son claves para tu análisis.
De acuerdo al análisis anterior y revisando la matriz de correlación se identifican las siguientes variables como las más representativas:
['location_key', 'date', 'country_code', 'country_name', 'new_confirmed',
       'new_deceased', 'cumulative_confirmed', 'cumulative_deceased',
       'cumulative_vaccine_doses_administered', 'population',
       'population_male', 'population_female', 'population_rural',
       'population_urban', 'population_density', 'human_development_index',
       'population_age_00_09', 'population_age_10_19', 'population_age_20_29',
       'population_age_30_39', 'population_age_40_49', 'population_age_50_59',
       'population_age_60_69', 'population_age_70_79',
       'population_age_80_and_older', 'gdp_usd', 'gdp_per_capita_usd',
       'latitude', 'longitude', 'area_sq_km', 
       , 'average_temperature_celsius',
       'minimum_temperature_celsius', 'maximum_temperature_celsius',
       'rainfall_mm', 'relative_humidity', 'population_largest_city',
       'area_rural_sq_km', 'area_urban_sq_km', 
       'new_recovered', 'cumulative_recovered'],

h) Guarda los datos filtrados en un archivo con el nombre DatosFinalesFiltrado.csv a fin de poder utilizarlo luego y no tener que repetir el proceso de filtrado y limpieza.
Se guardan los datos filtrados en la carpeta del proyecto.

![Picture6](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture6.png) 

i)Aplica bucles for y/o while para el cálculo de estadísticas descriptivas y otras métricas importantes que ofrece pandas por default.
Utilizando for generamos el siguiente bucle:




Utilizando while generamos el siguiente bucle: 

![Picture8](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture8.png) 

j)¿Qué implican estas métricas y cómo pueden ayudar en el análisis de datos?
Las métricas nos ayudan a consolidar las mediciones en los diversos pasos del analisis para le gestión de la calidad de los datos.
*¿Se muestran todas las estadísticas en todas las columnas durante el análisis?
En el siguiente pantallazo podemos ver las estadísticas que no genera pandas.

![Picture9](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture9.png)

Crea una función que permita obtener la mediana, varianza y el rango. Te dejamos algunas preguntas para analizar esas medidas:

¿Qué representa la mediana?
Es el numero intermedio de un grupo de números. Mide la tendencia central, que es la ubicación del centro de un grupo de números en una distribución estadística.


k)Cómo varía la dispersión de los datos en el conjunto de datos analizado, en términos de la varianza y el rango? En el siguiente grafico de Gauss podemos ver la distribución de los datos para la variable “new_confirmed” para Brasil.

![Picture10](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture10.png) 

¿Qué nos puede indicar esto sobre la consistencia o la variabilidad de los datos en relación con la 
mediana? En el siguiente grafico de Gauss podemos ver la distribución de los datos para la variable “new_deceased” para Brasil.

![Picture11](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture11.png) 

2.- AVANCE 2 
Las visualizaciones que puedes realizar son:
a) Gráficos de barras de países contra el resto de las variables. En el siguiente grafico se muestran todas variables de forma independiente en el histograma de frecuencia.

![Picture12](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture12.png)

b) Matriz de correlación, trata de crear una submascara para solo tomar una parte del gráfico y filtrar por los valores mayores a 0.5.      En la siguiente grafica podemos observar la correlación de las variables numéricas > .5 y  > -.5. Este análisis nos ayudo a seleccionar las variables mas representativas.                                                                                                                        
![Picture13](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture13.png) 

c)Diagrama de dispersión de la temperatura media contra los casos confirmados. En el siguiente diagrama podemos ver la distribución de los datos para las variables: “average_temperature_celcius” y “new_confirmed”.

![Picture14](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture14.png)


d)Diagrama de dispersión de la temperatura media contra las muertes confirmadas. En el siguiente diagrama podemos ver la distribución de los datos para las variables: “average_temperature_celcius” y “new_deceased”. 
						d.1
![Picture15](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture15.png) 


e) Dosis administradas por país ( BoxPlot). En el siguiente diagrama podemos ver la distribución de los datos para la variable: “cumulative_vaccine_doses_administered”.

![Picture16](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture16.png) 

f) Violinplot de las variables “human_development_index”,gdp_usd y cumulative_deceased para todos los países.
					f.1


g) Mapa de calor para mostar la correlación de variables.En este diagrama se observa la correlación de las variables: “population_urban”,“population_urban”,“cumulative_vaccine_doses_administered”

![Picture17](Desktop/PROYECTO_LABORATORIOS_COVID19/IMAGENES/Picture17.png)




      
















  


