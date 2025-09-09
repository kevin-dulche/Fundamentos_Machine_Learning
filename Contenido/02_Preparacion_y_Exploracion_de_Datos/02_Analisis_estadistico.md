# Análisis estadístico del rendimiento de un equipo de fútbol

## Resumen

El análisis del rendimiento de un equipo de fútbol requiere, antes que nada, una buena interpretación del pasado para entender el presente. Usando herramientas estadísticas básicas y visualizaciones efectivas, podemos extraer valiosas pistas que expliquen por qué un equipo triunfa o tiene dificultades. Concretamente, empleando bibliotecas como pandas, Matplotlib y seaborn, analizamos datos reales del equipo Cebollitas en diferentes condiciones de juego para obtener una visión clara sobre su desempeño.

## ¿Cómo obtener rápidamente información fundamental sobre los partidos?
Una de las maneras más eficaces para comenzar a entender los datos de partidos es mediante funciones básicas en Python. Para ello:

* Conviene siempre comenzar con la función `.head()`, que por defecto muestra cinco registros, pero permite ver más ajustando el parámetro.
* El método `.describe()` ofrece un resumen instantáneo, mostrando datos como promedio, mínimo, máximo y percentiles, facilitando el análisis fundamental del rendimiento del equipo.

Usando estas herramientas se obtiene información clara sobre promedio y máximos en situaciones esenciales, como los goles y los tiros al arco.

## ¿Es Cebollitas mejor jugando como local o visitante?
Conociendo el promedio de goles en cada condición podemos identificar fortalezas claras:

* De local, Cebollitas promedia 2.2 goles.
* Cuando juega de visitante aumenta notablemente a 2.6 goles, lo que indica un desempeño superior fuera de casa.

Este hallazgo, obtenido al usar promedios simples, puede mostrar aspectos claves para planteamientos tácticos.

## ¿Cómo interpretar la distribución de goles y detectar resultados extremos?
Distribuciones visuales mediante histogramas permiten descubrir:

* Frecuencias altas para resultados de dos, tres o cuatro goles jugando en casa.
* Muchos partidos sin goles y varios de alta anotación (hasta cinco goles) jugando como visitante.

Además, al utilizar gráficas de caja o boxplots, podemos detectar claramente resultados extremos (goleadas y derrotas notables), indicando un rendimiento frecuente entre un gol y cuatro goles, pero ocasionales resultados atípicos que merecen especial atención.

## ¿Existe relación entre la posesión del balón y los goles marcados?
Una gráfica scatterplot de posesión contra goles refleja:

* Resultados variados al tener aproximadamente 45% de posesión, sin mostrar una correlación claramente positiva.
* El dominio del balón parece no estar directamente relacionado con mayor anotación, mostrando la complejidad de esta relación y la necesidad de continuar explorando otras variables explicativas.

## ¿Qué variables presentan mayor correlación con el rendimiento?
A través de un mapa de calor o heatmap de correlaciones identificamos:

* Una correlación leve (0.17) entre goles marcados como local y posesión del balón.
* Ausencia de correlaciones fuertes (cercanas a 0.50 o mayores), indicando que ninguna de las variables tiene un poder explicativo evidente y se deberían profundizar otras estadísticas.

La correlación entre variables ofrece pistas iniciales, aunque limitadas, y abre la puerta para el desarrollo posterior de modelos predictivos más sofisticados.

La interpretación adecuada de estadísticas descriptivas y su representación visual permiten comprender cómo juegan los equipos y abren el camino para desarrollar modelos capaces de predecir resultados futuros de partidos deportivos.