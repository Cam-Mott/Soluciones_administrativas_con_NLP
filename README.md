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
Tanto el modelo a partir de BoW como TF-IDF presentan valores de accuracy, precision, recall y f1 
mayores a 0.90. Los mismos son presentados a partir de la función classification_report de la biblioteca
sklearn.metrics. Paralelamente se calcula el parámetro "Sentitive" para determinar la presencia o 
no de overfitting. 
