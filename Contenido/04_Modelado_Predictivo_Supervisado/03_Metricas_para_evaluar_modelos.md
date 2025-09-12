# Métricas para evaluar modelos de Machine Learning en predicciones

## Resumen

Evaluar los resultados de cualquier modelo de machine learning es crucial para determinar si puede emplearse en decisiones prácticas, sobre todo en entornos que exigen precisión, como el ámbito deportivo. Por eso, conocer métricas claras y específicas proporciona información objetiva sobre el rendimiento del modelo, identificando fortalezas y puntos a mejorar.

## ¿En qué consiste la evaluación de un modelo de Machine Learning?
Evaluar un modelo es muy parecido a examinar el desempeño deportivo de un jugador: interesa saber cuán certeros son sus movimientos y decisiones durante el juego. Con los modelos sucede igual, no basta con crear predicciones, es fundamental medir qué tan precisas son.

Las métricas más utilizadas son:

* **Error Cuadrático Medio (MSE)**: mide errores amplificados para destacar grandes desvíos.
* **Raíz del Error Cuadrático Medio (RMSE)**: devuelve el error a la escala original, facilitando la interpretación.
* **Error Absoluto Medio (MAE)**: muestra directamente el promedio real de errores, siendo robusto ante outliers.
* **Coeficiente de determinación (r al cuadrado)**: indica qué porcentaje de variabilidad explica el modelo respecto a la realidad.

## ¿Por qué es importante usar varias métricas al evaluar?
Utilizar un conjunto de métricas es crucial para formarse una idea clara y completa del funcionamiento del modelo:

* El **MSE** y **RMSE** detectan rápidamente grandes errores en predicciones específicas.
* El **MAE** aporta una visión directa y clara del error promedio.
* El **r al cuadrado** indica efectivamente la cantidad total de variabilidad explicada por el modelo.

Esta combinación brinda una evaluación integral, imprescindible para la toma informada de decisiones.

## ¿Cómo se calculan y visualizan estas métricas?
Para cuantificar estos aspectos:

1. Se importan bibliotecas esenciales como `pandas`, `NumPy` y `scikit-learn`.
2. Se define claramente la variable objetivo (por ejemplo, diferencia de goles) y las variables de entrada (tiros al arco, posesión del balón).
3. Se divide el set de datos con `train_test_split`.
4. Se entrena un modelo, en este caso una regresión lineal, y se generan predicciones.
5. Se calculan métricas clave con bibliotecas especializadas como mean squared error, mean absolute error y r2.

Finalmente, se realiza un análisis visual mediante un histograma de residuos, el cual permite detectar rápidamente sesgos o problemas específicos del modelo, determinando si tiende a sobreestimar o subestimar de manera constante.

## ¿Cómo interpretar los resultados de la evaluación visual e interactiva?
La evaluación interactiva, utilizando widgets en Jupyter, proporciona control directo sobre las expectativas del club o entrenador. Esto permite:

Buen control del umbral aceptable para errores medios.
Interacción dinámica con los resultados obtenidos y registrados.
Detectar un MAE elevado o un valor bajo de r al cuadrado sugiere revisar factores críticos, como calidad de datos, variables elegidas o la técnica de modelado seleccionada.