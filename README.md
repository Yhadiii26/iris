# iris
Preparación de Datos
El análisis comienza cargando el conjunto de datos IRIS.csv en un DataFrame de pandas.

Detección de duplicados: El código se encarga de identificar y eliminar 3 filas duplicadas, lo que reduce el total de 150 a 147. Este paso es clave para asegurarnos de que el modelo no se entrene con datos redundantes, lo que podría sesgar los resultados.

Verificación de nulos: Se confirma que el dataset no tiene valores nulos, lo que significa que no es necesario realizar ninguna imputación de datos.

Normalización: Las variables numéricas (sepal_length, sepal_width, petal_length, petal_width) se normalizan utilizando StandardScaler. Este paso es fundamental para el algoritmo K-Means, ya que lo hace menos sensible a las diferencias en las escalas de las variables.

Modelado y Análisis de Clustering
El código aplica el algoritmo K-Means con 3 clústeres (n_clusters=3), un número lógico dado que el dataset contiene 3 especies de flores. Los resultados del clustering se asignan a una nueva columna llamada cluster en el DataFrame.

El análisis de correspondencia entre los clústeres generados y las especies originales revela los siguientes hallazgos:

Clúster 1 vs. Iris-setosa: El código evalúa la correspondencia entre el cluster 1 y la especie Iris-setosa. Se observa que 48 de las flores Iris-setosa fueron asignadas a este clúster, lo que sugiere una alta precisión.

Clúster 0 vs. Iris-versicolor: Al analizar la correspondencia entre el cluster 0 y la especie Iris-versicolor, se encuentra que 39 flores de esta especie se agruparon en este clúster.

Clúster 2 vs. Iris-virginica: Finalmente, el código verifica la relación entre el cluster 2 y la especie Iris-virginica, mostrando que 36 flores de esta especie se asignaron a dicho clúster.
