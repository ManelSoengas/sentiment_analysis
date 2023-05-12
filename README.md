# sentiment_analysis
Se utiliza como datset un conjunto de datos basado en tewets que opinan en relación a una compañia aerea. Cabe decir el procedimiento es aplicable a cualquier conjunto de datos que contenga cómo mínimo un texto y una valoración. A partir de éste conjunto de datos hay que pre-procesar los datos y adaptarlos al formato adecuado para que el sistema pueda entrenar y aprender para crear un modelo. Los datos estan en ingés, pero es aplicable a cualquier idioma, pero hay que cargar previamente el idoma correspondiente.
```
# Carga del cojunto de datos
import pandas as pd
df = pd.read_csv("/content/Tweets.csv")
```
Visualización de la estructura y características de los datos.
```
# Visualización de una parte del data_frame
review_df = df[['text','airline_sentiment']]

print(review_df.shape)
review_df.head(5)
```
```
# Longitud y tamaño del conjunto de datos que interesa procesar.
# En éste caso el texto y la polaridad de la opinión.
review_df = review_df[review_df['airline_sentiment'] != 'neutral']

print(review_df.shape)
review_df.head(5)
```
```
# Cantidad de las etiquetas que definen la polaridad
review_df["airline_sentiment"].value_counts()
```
