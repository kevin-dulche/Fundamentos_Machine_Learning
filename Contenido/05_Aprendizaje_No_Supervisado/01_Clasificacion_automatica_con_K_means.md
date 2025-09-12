# Clasificación automática de jugadores con K-means clustering

## Resumen

El aprendizaje no supervisado, mediante la técnica de K-means, nos permite clasificar jugadores según características relevantes como goles, asistencias, pases completados y tiros al arco. Al utilizar esta técnica, los jugadores se agrupan de manera autónoma en perfiles estratégicos naturales, dejando que sean sus propias estadísticas las que definan roles específicos dentro del equipo.

## ¿Qué significa aprendizaje no supervisado y cómo lo estamos utilizando?
Anteriormente, los modelos aprendían mediante ejemplos etiquetados, ahora con el aprendizaje no supervisado, específicamente con el algoritmo K-means, los jugadores se agrupan automáticamente según características comunes. Por ejemplo:

* Delanteros con alto volumen de goles.
* Volantes creativos con muchas asistencias y pases.
* Defensores equilibrados.

Estos agrupamientos surgen sin etiquetas previas, revelando similitudes naturales en los datos que antes quedaban desapercibidas.

## ¿Cómo funciona exactamente el algoritmo K-means?
K-means asigna individuos a grupos o "clusters" basándose en proximidad matemática, realizando los siguientes pasos:

1. Elegir el número de grupos o "clusters".
2. Asignar cada dato al grupo cuyo centroide sea más cercano.
3. Recalcular los centroides y repetir hasta lograr estabilidad.

Al finalizar, jugadores con comportamientos estadísticos similares se encontrarán agrupados juntos, facilitando análisis adicionales y estrategias específicas.

## ¿Qué pasos seguimos en el notebook para clasificar jugadores?

* Importamos el dataset y verificamos sus columnas usando pandas.
* Visualizamos patrones estadísticos con gráficos interactivos mediante herramientas como seaborn y matplotlib.
* Aplicamos el algoritmo utilizando la biblioteca Scikit Learn.
* Verificamos las etiquetas generadas y realizamos visualizaciones gráficas para interpretar mejor los grupos obtenidos.

## ¿Qué información estratégica nos ofrece la agrupación de jugadores?
Esta clasificación por grupos permite tomar decisiones tácticas más acertadas, tales como:

* Adaptar entrenamientos individuales según perfiles específicos.
* Ajustar alineaciones para maximizar el rendimiento durante partidos.
* Detectar necesidades específicas para futuros fichajes.

Por ejemplo:

* **Grupo de delanteros**: alto promedio de goles y tiros al arco, dirigido hacia la efectividad ofensiva.
* **Volantes creativos**: destacándose en asistencias y pases completados, vitales en la construcción del juego.

## ¿Cómo mejorar o ajustar los resultados obtenidos con K-means?
Utilizando herramientas interactivas como widgets, se puede modificar la cantidad de grupos elegidos y observar variaciones en tiempo real. Esto permite explorar cuál es el número de perfiles óptimos y más útiles según la composición y necesidades particulares del equipo.

La agrupación automática basada en datos estadísticos redefine la forma en que un club entiende a sus jugadores, permitiendo descubrir habilidades y roles que antes estaban mezclados y poco claros.