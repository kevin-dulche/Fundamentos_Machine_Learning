# Selección de características con SelectKBest y árboles de decisión

## Resumen

Para lograr modelos predictivos eficientes, resulta clave elegir cuidadosamente las variables que aportan valor real. La selección de características, o feature selection, es un proceso que permite identificar las variables más relevantes, lo que mejora nuestras predicciones, reduce ruido y simplifica considerablemente el modelo.

## ¿En qué consiste realmente la selección de características?
La selección de características implica quedarse exclusivamente con variables que tienen una alta relevancia predictiva y eliminar aquellas que no aportan valor, disminuyendo así el ruido en el modelo. Menos variables, bien escogidas, permiten evitar sobreajustes y obtener predicciones más precisas.

## ¿Cómo funciona la selección univariada con SelectKBest?
Utilizando la biblioteca Scikit Learn, el método SelectKBest permite identificar las variables más relevantes según su relación lineal individual con la variable objetivo. En este ejercicio práctico se realiza lo siguiente:

* Se importan los métodos SelectKBest y f regression.
* Se calcula el puntaje F o F-score, indicando la influencia de cada variable sobre la variable objetivo (goles locales).
* Se evalúan todas las candidatas y se seleccionan las que obtienen mayores puntuaciones.

Las variables destacadas en este método fueron el porcentaje de posesión local, el ratio de tiros respecto a la posesión local y los tiros al arco locales.

## ¿Qué relevancia tiene un árbol de decisión en la selección de variables?
Los árboles de decisión, mediante Scikit Learn y su método DecisionTreeRegressor, permiten capturar tanto relaciones no lineales como interacciones entre variables. Estos son los pasos esenciales:

* Se crea un modelo de árbol que divide las variables para minimizar el error cuadrático en la variable objetivo.
* Se define la importancia de cada característica según su aporte a la reducción en errores o impurezas.
* Se comparan variables según la importancia calculada por el modelo.

En este ejercicio, nuevamente resaltaron por relevancia la posesión local, el ratio de tiros respecto a posesión local y los tiros al arco local.

## ¿Cuál técnica es mejor para seleccionar variables?
Ambas técnicas, selección univariada y árboles de decisión, proporcionan perspectivas diferentes pero complementarias. Al realizar una visualización comparativa gráfica con barras, queda en evidencia:

* El comportamiento de ambas técnicas es similar.
* Aunque puntajes y valores de importancia son diferentes en magnitud, concluyen coincidiendo sobre las variables más relevantes.

Reducir variables seleccionando cuidadosamente las más relevantes permite obtener buenas predicciones, al tiempo que simplifica y mejora el modelo. Variables clave identificadas como ratio de tiros sobre posesión y posesión local muestran gran potencial predictivo en este contexto específico.