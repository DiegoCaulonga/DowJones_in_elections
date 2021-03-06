![Captura de pantalla 2020-11-18 a las 16 19 55](https://user-images.githubusercontent.com/69120593/99549429-ebff5580-29b9-11eb-8b35-c14891720333.png)



# DowJones_in_elections
Bienvenidos a mi estudio sobre el comportamiento del Dow Jones despúes de las distintas elecciones americanas a lo largo de la historia. Teniendo en cuenta que estamos en año de elecciones en EEUU, y que con las constantes oscilaciones de los mercados de valores debido a la situación mundial, la afición por la inversión se ha generalizado, he decidido hacer un estudio a cerca del comportamiento del Dow Jones los años posteriores al nombramiento de presidentes en "el gran pais". Para poneros un poco en contexto, por un lado hay que saber que las elecciones en EEUU se hacen, siempre, cada cuatro años, el primer martes después del primer lunes de Noviembre (si el Martes cae en día 1, las elecciones serían la semana siguiente, al caer el lunes en 31 de Octubre). Por otro lado, el Dow Jones, es el índice mas representativo de la bolsa americana. Nació en 1896, y mide el desempeño de las 30 empresas mas grandes que cotizan en el mercado bursatil de EEUU. Históricamente, y por lo general, se ha compuesto por empresas industriales, aunque con el auge de las tecnológicas, varias empresas del NASDAQ han sido introducidas dentro de este gran índice en los ultimos años (y el número seguro que irá creciendo). 
Por lo tanto, y sabiendo esto, me puse a investigar a cerca del comportamiento de este índice, los años posteriores a las elecciones en Estados Unidos, cuando el presidente lleva un par de meses electo, ingresa en la Casa Blanca, y comienza su presidencia. 
Para los que estén familizariados con Python3, y les interese, ire adjuntando los links de cada paso donde se puede ver el codigo que he ido escribiendo.

## Presidents (https://github.com/DiegoCaulonga/DowJones_in_elections/blob/main/Presidents.ipynb)
En este primer paso, utilizando webscraping (obtención de datos de internet utilizando un link y su html), obtube una tabla en la que se recogía el histórico de presidentes de estados unidos, sus nombres, el año en el que fueron electos, y el partido al que pertenecían. La tabla la podeis encontrar arriba, en presidents.csv.

## Dow Jones (https://github.com/DiegoCaulonga/DowJones_in_elections/blob/main/DowJones.ipynb)
En el segundo paso, y tambien utilizando webscraping, obtube la tabla en la que se representa la evolución del Dow Jones año a año, con una columna en la que se ve el año (comenzando en 1915) y otra columna donde se ve la fluctuacion anual. Esta tabla también la podeis encontrar arriba, se llama DowJones.csv.

## Analysis (https://github.com/DiegoCaulonga/DowJones_in_elections/blob/main/Analysis.ipynb)
Aunque el nombre no concuerde exactamente con lo hecho en este código, en mi tercer paso mi objetivo fue limpiar las dos tablas obtenidas anteriormente, para obtener una tabla en la que se representaran los años de elecciones, los presidentes electos, los partidos a los que pertenecían, y las fluctuaciones del Dow Jones durante el año posterior a las respectivas elecciones. 
![Captura de pantalla 2020-11-18 a las 13 17 22](https://user-images.githubusercontent.com/69120593/99530525-b6e70900-29a1-11eb-8a77-bfca3f652ed2.png)

## Graph Creation (https://github.com/DiegoCaulonga/DowJones_in_elections/blob/main/GraphCreation.ipynb)
En este último paso me dediqué a generar una serie de representaciones gráficas, utilizando la librería matplotlib, para poder visualizar mejor los datos obtenidos en la tabla.

### Históricos en barras
Para estos cálculos, he filtrado la tabla de arriba por la columna de "Presidents Party", para ver los resultados según este dato que he considerado discriminante durante todo el trabajo. Las tablas obtenidas serían RepublicanHist.csv y DemocratHist.csv, ubicadas en la carpetata OutPut. Las podeis ver en este link: https://github.com/DiegoCaulonga/DowJones_in_elections/tree/main/OutPut
Las representaciones gráficas de las tablas serían las siguientes:     
![Captura de pantalla 2020-11-18 a las 14 25 38](https://user-images.githubusercontent.com/69120593/99536037-13e6bd00-29aa-11eb-9097-736560be5da5.png)
![Captura de pantalla 2020-11-18 a las 14 26 02](https://user-images.githubusercontent.com/69120593/99536074-1fd27f00-29aa-11eb-9355-d15755bc18bd.png)

En estas gráficas, podemos observar que por lo general, los resultados durante el primer año de presidencias demócratas, han sido más positivos. Tienen el año con mejor resultado (1932), pero también el año con peor resultado (1936), que supera de maner negativa incluso al Crack del 29, que ocurrió durante el primer año de presidencia del presidente republicano Herbert Huber. 


### Media en barras
![Captura de pantalla 2020-11-18 a las 13 36 51](https://user-images.githubusercontent.com/69120593/99531539-2c9fa480-29a3-11eb-97ff-edbbbeea9a64.png)

Este gráfico de barras representa la media de fluctuaciones según el partido del presidente electo. Podemos apreciar que la media de fluctuaciones del Dow Jones durante el primer año de presidencia, tiene resultados positivos con ambos partidos, aunque con una diferencia bastante favorable para los democratas, de casi un 8%.

### Resultos positivos y negativos
Pata hacer estos calculos he generado una columno con numeros binarios, haciendo referencia a cuando los partidos politicos, para calcular si la cantidad de veces que el resultado del primer año de presidencia era positivo o negativo en cuanto al Dow Jones se refiere.
![Captura de pantalla 2020-11-18 a las 15 57 43](https://user-images.githubusercontent.com/69120593/99546633-eb18f480-29b6-11eb-98c8-bfd88720f17a.png)
![Captura de pantalla 2020-11-18 a las 15 57 52](https://user-images.githubusercontent.com/69120593/99546836-23203780-29b7-11eb-800b-032c06b13d64.png)

Es donde mayores diferencias he observado, viendo que los emocratas se llevan esta estadistica con creces, teniendo mas resultados positivos, aun habiendo tenido menos representantes presidenciales (desde el origen del Dow Jones).


## CONCLUSIÓN
Aunque está claro que los resultados referentes al Dow Jones durante la historia del año 1 de presidencia en EEUU son bastante favorables a los demócratas, no hay que pasar por alto, que este estudio solo recoge un 25% de los datos totales del Dow Jones, o lo que es lo mismo, que los presidentes ejercen como tal durante 4 años, y no solo 1, por lo que no hay que sacar conclusiones precipitadas. Más adelante, realizaré un estudio en el que se recojan los datos de todos los años, y no solo el primero de cada presidencia, para contrastar datos y ver si las diferencias varían. Este estudio lo he realizado ya que me parecia interesante ver que puede pasar en este proximo año 1. La situación mundial es muy inestable, y las predicciones que un algoritmo de Machine Learning pudiera proporcionarnos, no iban a tener en cuenta que existe un virus fastidiando la economia mundial, por lo que sabiendo eso, y que la oficialidad de Biden como presidente no es absoluta, he preferido no calcular ese dato. 

LLegado a este punto, te agradezco que hayas leído mi estudio, y no me importaría que me dejaras como comentario en la publicación de LinkedIn, alguna recomendación que te pudiera interesar sobre algún estudio que pueda hacer. 
![Captura de pantalla 2020-11-18 a las 16 13 58](https://user-images.githubusercontent.com/69120593/99548589-1ac8fc00-29b9-11eb-8227-2b116f9ce440.png)



