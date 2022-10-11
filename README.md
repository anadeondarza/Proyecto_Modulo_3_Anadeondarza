##Proyecto módulo 3

Este es el README de mi tercer proyecto en Ironhack. El proyecto consiste en realizar la compety de diamantes de Kaggle con el objetivo de crear nuestro modelo supervisado para predecir el precio de los diamantes. 

##EDA📌

Tras realizar el análisis de nuestro Data Set, podemos observar que las features que más inciden en el precio son las referentes a su tamaño y volumne, esdecir, X, Y, Z, y el carat. Además, el carat y el volumen tienen una relación directa. 
El precio del diamente depende de su Volumen, y de sus carat principalmente, a mayor volumen, mayor carat, mayor precio. 

Estas 4 features tienen outlayers, únicamente vamos a quitar el outlayer del features Volumen, X, Y y Z para quitar esta "distorsión".

Las features que menos peso tienen en el precio son la ciudad, el color, la claridad, y el corte. 


##Best Model 💻

1. El mejor RMSE en Kaggle: 584.27665 / Notebook 541.060

Descripción del modelo:
Paso 1: Separamos el precio del resto de features.
Paso 2: Creamos la nueva vfeature Volumen, multiplicado las features relacionadas con el tamaño. 
Paso 3: Posteriormente separamos las variables cualitativas de las numéricas, y trabajamos con ellas por separado.
Paso 4: Escalamos las features numéricas utilizando el StandardScaler, y lo pasamos de nuevo a Dataframe. 
Paso 5: Convertirmos las features cualitativas a numericas con el label_encoder para posteriormente escalarlas de nuevo con el StandardScaler. 
Paso 6: Una vez que tenemos nuestros Dataframes los unimos con un merge y entrenamos el modelo sobre ese Dataframe. 
Paso 7: Para entrenarlo aplicamos al Dataframe el train_test_split para poder poder trabajar con el X_train y aplicarlo a X_test. 
Paso 8: Aplicamos el RandomForestRegressor, el modelo que mejor RMSE nos ha dado. Para los parámetros hemos utilizado parámtros tipo. 
Paso 9: Posteriormente aplicamos el mismo trabajo el al dataset para el que queremos predecir. 


2. El mejor de mis notebook: 542.73

Descripción del modelo:
Paso 1: Separamos el precio del resto de features.
Paso 2: Creamos la nueva vfeature Volumen, multiplicado las features relacionadas con el tamaño. 
Paso 3: Posteriormente separamos las variables cualitativas de las numéricas, y trabajamos con ellas por separado.
Paso 4: Escalamos las features numéricas utilizando el StandardScaler, y lo pasamos de nuevo a Dataframe. 
Paso 5: Convertirmos las features cualitativas a numericas dando más peso a las que en el EDA hemos visto que estan relacionadas con un precio mayor y las escalamos con StandardScaler, y las pasamos a Dataframe. 
Paso 6: Una vez que tenemos nuestros Dataframes los unimos con un merge y entrenamos el modelo sobre ese Dataframe. 
Paso 7: Para entrenarlo aplicamos al Dataframe el train_test_split para poder poder trabajar con el X_train y aplicarlo a X_test. 
Paso 8: Aplicamos el RandomForestRegressor, el modelo que mejor RMSE nos ha dado. Para los parámetros hemos utilizado parámtros tipo. 
Paso 9: Posteriormente aplicamos el mismo trabajo el al dataset para el que queremos predecir. 

##Analysis ✒️

Tras la realización del modelo, y tras el intento de multiples análisis, he podido comprobar que la reducción de features, quitando las que menos peso tienen no mejora las predicciones.
El RandmForest es el que nos ofrece mejor predicciones, el RMSE más bajo. 

El trabajo por separado de las variables númericas y cualitativas nos da un mejor RMSE.
