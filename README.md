# Plan de trabajo

[Google Drive](https://drive.google.com/drive/folders/17FhWbmf-yrM_O8_6QcMLvTLurjviZqyu)

[Modelo](https://www.kaggle.com/datasets/lehaknarnauli/spotify-datasets)

[Base de datos](https://www.kaggle.com/datasets/yamaerenay/spotify-dataset-19212020-600k-tracks?resource=download)

## Presentación

[Reveal.js guide](https://quarto.org/docs/presentations/revealjs/)

## Reunión 0

- Leer los siguientes links para plantear ideas:
    - <https://www.kaggle.com/code/vatsalmavani/music-recommendation-system-using-spotify-dataset>
    - <https://www.kaggle.com/datasets/lehaknarnauli/spotify-datasets?resource=download&select=tracks.csv>
    - <https://datascience.fm/fun-analysis-of-spotify-dataset-to-gain-insights-on-music-industry/>

## Reunión 1

- Fijamos la base de datos a emplearse.

- [Modelo 1](https://adrian-mb97.medium.com/predicting-the-odds-a-song-of-reaching-the-billboard-hot-100-d48776da386b)

- [Modelo 2](https://github.com/jesperhemmingsson/Spotify-EDA)

- **Dudas** 
    - Dimensión apropiada del dataset.
    - ¿Se puede scrapear un dataset y 
    hacerle un merge con la data previamente descargada?
    - ¿El enfoque debe ser puramente predictivo? ¿Descriptivo también?
    - ¿El enfoque debe ser del tipo que trabajamos para una empresa?, como si fuese un cliente.
    - ¿Solamente planteamos un modelo, o podemos realizar diversos modelos en base a clusters de la data? 
    La idea de realizar diversos modelos (del mismo tipo pero para clusters distintos) es comparar si los resultados del mismo tipo de modelo son los mismo. 

- **Producto final**
    - `presentacion_1.html` 
    - `codes/limpieza-de-datos.html` 

## Reunión 1 con la profesora

### Preguntas para reunión con la profesora

1. ¿Es correcto realizar imputación a la variable por predecir? \
  Ans: No se imputa; generaría data fictica.
       Excluir la variable dependiente.

1. ¿Sería conveniente recategorizar (en **menos** valores) \
a la variable categórica **release_date**?
  Ans: Sí, check comments en notebook.

1. ¿Sugiere que cambemos de dataset? \
  Ans: No, pero explorar más las variables, sus combinaciones, etc.

1. Sobre `Descripción del universo y muestra (incluyendo descripción en espacio y tiempo)` \
  Ans:
      Universo: All songs in spotify which can be loaded via its API.
      Muestra: Lo recolectado en un rango temporal particular (find it).
      Util mencionar que la data es de Kaggle, pero que fue recolectada via Spotify's API.

1. Sobre `-Selección de registros y atributos` \
  Ans:
    registro: fila, atributo: columna
    No hemos filtrado filas a priori.

1. ¿Deberíamos generar modelos respecto a particiones de release_date? \
  Ans: Basta hacer un modelo general, al menos para este proyecto.
       En caso se analice por casos (temporales), podríamos aplicar
       un for loop para obtener los modelos en cada rango temporal.
       Aunque, idealmente, el análisis se realizaría más a detalle
       (como estamos haciendo en el caso general) para cada rango temporal,
       sea para fijar los cortes para datos atípicos, etc.

## Recomendaciones de sensei

- En caso que el modelo no llege a predecir tan bien la popularidad,
nos recomienda discretizar la variable numérica popularidad, en 5 
categorías, y hacer un modelo de clasificación. \
Pues, predecir variables numéricas suele ser más complicado
que predecir variables categóricas.

## Reu post meeting with Stefany sensei

### Preguntas

- ¿Es necesario estandarizar o normalizar cada una de 
las variables numéricas? ¿Debe haber algún criterio
para realizar tales transformaciones?

### Exploración respecto a longitud del nombre de la canción



## Bibliografía:

- https://ieeexplore.ieee.org/document/8999039
- https://towardsdatascience.com/song-popularity-predictor-1ef69735e380
- https://www.cdes.org.in/wp-content/uploads/2022/01/Predicting-Music-Popularity.pdf

