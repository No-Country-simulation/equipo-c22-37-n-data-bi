## Nombre de este equipo: 

c22-37-n-data-bi

## Vertical tecnológica del proyecto: 

Data - BI

## Nombre del proyecto:

InfoDataMind

## Coequipers:

- Mariana Valeria Isabel Villamayor - Data Analyst | mvillamayor099@gmail.com | Argentina
- Jesus Joaquín Cerón Melgoza - Data Analyst | jjcm@exatec.tec.mx | México

## Team Leader:

- Claudio Marcelo Fabian Castillo 

## Conjunto de datos utilizado:

Fuente: https://opendata.paho.org/en/core-indicators/download-dataset

El conjunto de datos de la Organización Panamericana de la Salud (PAHO por sus siglas en inglés) fue descargado el día 10 de diciembre de 2024, y su última actualización fue el día 18 de noviembre del presente año. El archivo original contiene 27 columnas, sin embargo, se ha decidido delimitar el análisis de datos a 5 columnas de datos y a 77 indicadores.

## Archivo CSV usado en Google Colab

El siguiente enlace permite descargar el archivo original que se utilizó en Google Colab:
https://drive.google.com/file/d/1FIjEM4FFgtJYa2h6nBFr3k89_RAkf05z/view?usp=sharing

## Descripción de los pasos de exploración, preparación y selección de los datos (etapa previa a la visualización de datos)

El primer paso fue escribir un bloque de código dentro de una celda en un archivo de Google Colab denominado “notebook”. El bloque de código correspondiente al primer paso contiene líneas de código para importar la librería pandas y permitir utilizar archivos, una función que permite subir archivos CSV a Google Colab, se utilizó el método df.info() para obtener un resumen del archivo CSV que permite mostrar la cantidad de valores no nulos de cada columna y se usó un ciclo con instrucciones que permitir ver los valores únicos y la cantidad de valores únicos de cada columna. El archivo original que se utilizó al ejecutar el bloque de código escrito en la celda se llama "PAHO-Core-Indicators-2024-20241126".

El segundo paso fue modificar el bloque de código de la celda del primer paso para que mediante instrucciones se seleccionaran 5 columnas relevantes para el análisis y la visualización de datos. El bloque de código del segundo paso además contiene instrucciones que permiten guardar el dataframe con las columnas seleccionadas. Cuando el bloque de código de la celda del segundo paso se terminó de ejecutar se obtuvo un archivo con el nombre "selected columns.csv".

El tercer paso fue desarrollar líneas de código que permitieran imprimir una lista de los valores únicos ordenados alfabéticamente de la columna 'spatial_dim_es' que contiene los países considerados en el conjunto de datos de la Organización Panamericana de la Salud. El bloque de código del tercer paso pide al usuario que suba el archivo "selected columns.csv" para poder imprimir la lista. Con este bloque de código observamos que la Organización Panamericana de la Salud obtuvo datos de 49 países del continente americano.

El cuarto paso fue reemplazar el valor 'Bolivia (Estado Plurinacional de)' de la columna 'spatial_dim_es' por Bolivia para que el software Tableau Public pudiera considerar a este país en una visualización de mapa. Cuando el bloque de código de la celda del cuarto paso se terminó de ejecutar se obtuvo un archivo con el nombre "corrected data.csv".

El quinto paso fue desarrollar líneas de código que permitieran ordenar alfabéticamente los valores únicos de las columna 'nombre_indicador' y mostar el id correspondiente de cada indicador.

El sexto paso consistió en modificar el bloque de código utilizado en la celda del tercer paso para imprimir la lista de los valores únicos ordenados alfabéticamente de la columna 'nombre_indicador' y así poder ver el nombre completo de cada indicador del archivo original de la Organización Panamericana de la Salud. El archivo original contiene 299 indicadores.

El séptimo paso fue escribir código para seleccionar manualmente los indicadores más relevantes para la visualización de datos de acuerdo a la decisión que el equipo tomó desde la semana cero la cual fue trabajar con indicadores relacionados con salud mental. El equipo decidió incluir los indicadores más relevantes de las enfermedades no transmisibles y otros indicadores para ampliar el análisis y así el producto mínimo viable sea interesante para usuarios potenciales. Cuando el bloque de código de la celda del séptimo paso se terminó de ejecutar se obtuvo un archivo con el nombre "indicadores seleccionados".

Finalmente se ejecutó un bloque de código para comprobar que el archivo con el nombre "indicadores seleccionados.csv" incluyera los indicadores elegidos.

Para poder ver los bloques de código utilizados en los 7 pasos acceda a través del siguiente enlace:
https://colab.research.google.com/drive/1E-hXVZr4ensX01czw8SwOu1LjUSn3j10?usp=sharing

## Explicación adicional de los pasos de exploración, preparación y selección de los datos

El archivo original contiene 327521 filas y el peso del archivo es de 125,631 KB. Los 7 pasos descritos anteriormente permitieron obtener un archivo con 112855 filas y un peso de 8527 KB. Como no tenemos amplia experiencia usando el software Tableau Public, desconocemos si sea posible cargar archivos de más de 100,000 KB (100 MB).

## Agrupación de indicadores

Hemos agrupado los 77 indicadores elegidos para que el dashboard interactivo en Tableau cuente con un número reducido de secciones.

Las secciones del dashboard interactivo son las siguientes:

1.-Indicadores de alfabetización en problemas de salud
* Años de escolaridad promedio (en años)
* Años de escolaridad promedio (en años); hombre
* Años de escolaridad promedio (en años); mujer
* Tasa de alfabetización en jóvenes (%)
* Tasa de alfabetización de jóvenes; hombre
* Tasa de alfabetización de jóvenes; mujer

2.-Indicadores de hábitos nocivos
* Consumo total de alcohol per cápita (15 años y más)
* Consumo total de alcohol per cápita (15 años y más); hombre
* Consumo total de alcohol per cápita (15 años y más); mujer
* Prevalencia de actividad física insuficiente en adolescentes (%)
* Prevalencia de actividad física insuficiente en adolescentes (%); hombre
* Prevalencia de actividad física insuficiente en adolescentes (%); mujer
* Prevalencia de actividad física insuficiente en adultos (%)
* Prevalencia de actividad física insuficiente en adultos (%); hombre
* Prevalencia de actividad física insuficiente en adultos (%); mujer
* Prevalencia del consumo actual de tabaco en adolescentes (%)
* Prevalencia del consumo actual de tabaco en adolescentes (%); hombre
* Prevalencia del consumo actual de tabaco en adolescentes (%); mujer
* Prevalencia del consumo actual de tabaco en adultos (%)
* Prevalencia del consumo actual de tabaco en adultos (%); hombre
* Prevalencia del consumo actual de tabaco en adultos (%); mujer

3.-Indicadores demográficos
* Población total (en miles)
* Población total (en miles) 0-1 años
* Población total (en miles) 0-1 años; hombre
* Población total (en miles) 0-1 años; mujer
* Población total (en miles) 1-4 años
* Población total (en miles) 1-4 años; hombre
* Población total (en miles) 1-4 años; mujer
* Población total (en miles) 15-24 años
* Población total (en miles) 15-24 años; hombre
* Población total (en miles) 15-24 años; mujer
* Población total (en miles) 25-44 años
* Población total (en miles) 25-44 años; hombre
* Población total (en miles) 25-44 años; mujer
* Población total (en miles) 45-64 años
* Población total (en miles) 45-64 años; hombre
* Población total (en miles) 45-64 años; mujer
* Población total (en miles) 5-14 años
* Población total (en miles) 5-14 años; hombre
* Población total (en miles) 5-14 años; mujer
* Población total (en miles) 65-74 años
* Población total (en miles) 65-74 años; hombre
* Población total (en miles) 65-74 años; mujer
* Población total (en miles) 75+ años
* Población total (en miles) 75+ años; hombre
* Población total (en miles) 75+ años; mujer
* Población total (en miles); hombre
* Población total (en miles); mujer

4.-Indicadores económicos del sector salud
* Ingreso nacional bruto (US$ per cápita), corriente internacional (ajustado PPA)
* Ingreso nacional bruto per cápita, método Atlas (US$ corriente)
* Producto interno bruto (US$ per cápita) internacional corriente (ajustado PPA)
* Gasto del bolsillo en salud como % del gasto corriente en salud
* Gasto privado en salud como % del PIB
* Gasto público en salud como % del PIB
* Inflación (%)

5.-Indicadores generales de salud
* Defunciones (en miles)
* Defunciones por enfermedades no transmisibles (%)
* Defunciones por enfermedades no transmisibles (%); hombre
* Defunciones por enfermedades no transmisibles (%); mujer
* Esperanza de vida al nacer (en años)
* Esperanza de vida al nacer (en años); hombre
* Esperanza de vida al nacer (en años); mujer
* Tasa de mortalidad general (ajustada por edad por 1 000 habs)
* Tasa de mortalidad general (ajustada por edad por 1 000 habs); hombre
* Tasa de mortalidad general (ajustada por edad por 1 000 habs); mujer
* Tasa de mortalidad por Alzheimer y otras demencias (ajustada por edad por 100 000 habs)
* Tasa de mortalidad por Alzheimer y otras demencias (ajustada por edad por 100 000 habs); hombre
* Tasa de mortalidad por Alzheimer y otras demencias (ajustada por edad por 100 000 habs); mujer
* Tasa de mortalidad por enfermedades no transmisibles (ajustada por edad por 100 000 habs)
* Tasa de mortalidad por enfermedades no transmisibles (ajustada por edad por 100 000 habs); hombre
* Tasa de mortalidad por enfermedades no transmisibles (ajustada por edad por 100 000 habs); mujer
* Tasa de mortalidad por suicidio (ajustada por edad por 100 000 habs)
* Tasa de mortalidad por suicidio (ajustada por edad por 100 000 habs); hombre
* Tasa de mortalidad por suicidio (ajustada por edad por 100 000 habs); mujer

6.-Indicadores sobre la densidad del personal de salud
* Densidad de farmacéuticos/as (10 000 habs)
* Densidad de médicos/as (10 000 habs)
* Densidad del personal de enfermería (10 000 habs)

