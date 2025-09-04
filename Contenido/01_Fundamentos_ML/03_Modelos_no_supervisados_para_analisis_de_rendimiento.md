# Modelos no supervisados para análisis de rendimiento deportivo

## Resumen

¿Alguna vez te has preguntado cómo evaluar al jugador que toca el balón muchas veces pero no realiza goles ni asistencias claras? En el fútbol moderno, entender el valor que un jugador aporta al equipo va más allá de las estadísticas tradicionales. Aquí es donde entran en juego técnicas avanzadas como los modelos no supervisados, proporcionando una nueva perspectiva en el análisis deportivo.

## ¿Qué es el clustering y cómo identifica estilos de juego?
El clustering es una técnica dentro de los modelos no supervisados que agrupa jugadores con rendimiento y estilos similares, sin necesidad de etiquetas previas como goles o asistencias. Por ejemplo, el algoritmo k-means divide los datos en grupos seleccionando un centro y colocando a los jugadores más parecidos en un mismo grupo. Esto permite descubrir perfiles específicos como carrileros incansables, mediocampistas de recuperación o incluso delanteros fantasmas.

## ¿Cómo funcionan otros algoritmos cuando los grupos no están claros?
Cuando los datos no muestran claramente cuántos grupos hay o la forma que tienen esos conjuntos, DBSCAN es una opción útil. Este algoritmo agrupa jugadores basándose en la densidad, identificando aquellos que se comportan parecido por su proximidad, aunque no formen figuras geométricas claras. Otra alternativa destacada es el clustering jerárquico, que crea dendrogramas agrupando jugadas o jugadores hasta formar categorías amplias.

## ¿Cómo visualizar datos complejos con reducción de dimensionalidad?
A menudo, los datos deportivos incluyen múltiples variables difíciles de visualizar directamente. Para esto sirve la reducción de dimensionalidad, destacando técnicas como PCA (análisis de componentes principales), que resumen la información en menos dimensiones, facilitando una visión global del rendimiento, similar a observar un partido desde un dron. Técnicas adicionales como T-SNE o UMAP permiten representar visualmente datos complejos en espacios reducidos (2D o 3D), revelando patrones escondidos.

## ¿Cómo validar agrupamientos sin etiquetas claras?
Validar resultados en modelos no supervisados es un desafío, al no contar con etiquetas claras como goles o asistencias ganadoras. Para evaluar agrupamientos, son útiles métricas como:

* **Inercia**: indica qué tan compactos son los grupos.
* **Coeficiente de silhouette**: evalúa qué tan bien separados están los grupos.

Estas métricas ofrecen señales para entender si los grupos detectados tienen sentido o son producto de una aparente casualidad.