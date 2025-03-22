# Soluciones-administrativas-con-NLP
## **Introducción**
En el ámbito de la administración surgen diversas problematicas, entre ellas
clasificar los egresos por categoría. Este trabajo suele ser manual y tedioso: se 
debe leer concepto por concepto y elegir la categoría correspondiente. La propuesta 
presentada consiste en aplicar dos herramientas de la ciencia de datos:
los **modelos de clasificación** y las técnicas de **procesamiento de lenguaje natural**.
Mediante dos modelos, **RandomForestClassifier** y las técnicas **Bag of Word** y **TF-IDF**
se buscará codificar los conceptos en vectores numéricos, para luego utilizar
los mismos como input de un modelo de clasificación, cuya salida sean las categorías
correspondientes.

## **Datasets**
El dataset proviene de una empresa real, cuya razón social no se revelará por motivos de confidencialidad. Sin embargo, la planilla 
esta disponible en google sheets y es de libre acceso. En la misma se puede observar las columnas "fecha", "concepto" y "categoría".
Las columnas "ingreso" y "egreso" fueron eliminadas por las mismas razones de confidencialidad. 

## **Métricas**
Tanto el modelo basado en BoW como en TF-IDF presentan valores de accuracy superiores a 0.98. 
Los mismos son presentados a partir de la función classification_report de la biblioteca
sklearn.metrics. Paralelamente se calcula el parámetro "Specifity" para determinar la presencia o 
no de overfitting. Podemos observar que tantos las métricas **presicion** como **recall** también 
presentan valores altos. Si bien valores altos de dichas métricas puede ir de la mano con un 
modelo que solo predice valores positivos, lo cual disminuye las predicciones false negative (incrementando 
por ende el **recall**), ambos modelos presentan altos valores de **specificity** (cercanos a uno) por 
lo que los modelos son buenos también en las predicciones de negativos.
