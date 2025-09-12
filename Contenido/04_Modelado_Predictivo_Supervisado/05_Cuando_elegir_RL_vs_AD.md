# Cuándo elegir regresión lineal vs árboles de decisión

## Resumen

La elección adecuada de un modelo de predicción depende directamente de la naturaleza y comportamiento de nuestros datos. Al explorar la regresión lineal y el árbol de decisión, observamos diferencias significativas en sus resultados y métricas de desempeño. Analicemos juntos estos resultados y sepamos cuándo conviene seleccionar cada alternativa.

## ¿Por qué falló la regresión lineal en este caso?
Al revisar el modelo de regresión lineal, notamos un valor negativo en la métrica R². Esto indica que nuestra predicción es menos efectiva que simplemente utilizar el promedio de los datos como referencia. Claramente, el modelo lineal no está capturando la esencia del patrón de nuestros datos, revelando una buena pista: la relación entre las variables involucradas no es lineal.

## ¿En qué destaca el modelo de árbol de decisión?
Al probar el modelo basado en un árbol de decisión, advertimos mejoras significativas, especialmente:

* Menor error en RMSE y MAE.
* Mayor valor en la métrica R², lo que implica una capacidad más efectiva de explicar la variabilidad en nuestros datos.

Esto significa que el árbol de decisión es más adecuado en este escenario particular, al adaptarse con más precisión al comportamiento no lineal que presentan las variables.

## ¿Cómo interpretar las métricas y su impacto en la elección del modelo?
Las métricas proporcionan señales claras acerca de qué tan adecuado es un modelo. En este caso específico:

* Un R² negativo indica desempeño peor que la media como predictor.
* La reducción significativa en los valores de RMSE y MAE confirma la precisión superior del árbol de decisión.

Al entender el significado de estas métricas, seleccionamos modelos que aprovechan el verdadero potencial predictivo de nuestros datos.

## ¿Qué aprendemos y qué estrategias seguir hacia adelante?
Este análisis resalta aspectos clave del trabajo con modelos predictivos:

* No todos los algoritmos funcionan bien en todos los escenarios.
* La preparación adecuada de datos y la selección de métricas precisas son fundamentales.
* El uso efectivo de los modelos depende del entendimiento detallado del comportamiento de los datos.

Hacia adelante, podemos considerar estrategias como:

* Redefinir y mejorar nuestro pipeline.
* Incrementar la calidad de representaciones gráficas en visualizaciones.
* Probar nuevos modelos, más robustos, que se alineen aún más con la naturaleza de nuestros datos.

Este enfoque consciente mejora sustancialmente nuestras posibilidades de alcanzar resultados precisos y prácticos en proyectos futuros.