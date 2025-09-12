# Creación de modelos de regresión lineal para predecir goles

## Resumen

¿Quieres aprender cómo predecir resultados deportivos usando inteligencia artificial? Hoy comenzarás tu primer modelo de regresión lineal aplicado al deporte. Este es uno de los métodos clásicos y eficaces de aprendizaje automático, útil para relacionar variables relevantes con objetivos específicos, como la diferencia de goles en un partido.

## ¿Cómo preparamos el modelo para predecir goles?
Primero se importan herramientas esenciales como `pandas` y `train_test_split`. Con estas herramientas, cargamos y preparamos el conjunto de datos, definiendo claramente nuestra variable objetivo: la diferencia de goles entre equipos locales y visitantes. Adicionalmente, se escogen variables clave para hacer predicciones, como:

* Posesión del equipo local.
* Cantidad de tiros al arco del equipo local.

Se emplea la práctica recomendada de separar el conjunto de datos en entrenamiento y evaluación (80% y 20% respectivamente) con un `random_state` fijo, garantizando resultados reproducibles.

## ¿Qué ocurre al entrenar el modelo?
Usando la clase `LinearRegression` de scikit-learn, el proceso implica:

* Instanciar y entrenar el modelo mediante `modelo_rl.fit()`, optimizando los parámetros para minimizar el error cuadrático medio.
* Confirmar visualmente que el proceso de entrenamiento se realizó correctamente.

El intercepto y los coeficientes del modelo indican cómo reaccionan las predicciones ante cambios en las variables tomadas como predictores:

* Un incremento de un punto porcentual en posesión ajusta la diferencia de goles en promedio en 0.03.
* Un aumento en los tiros al arco afecta levemente negativamente (en promedio -0.37).

Estas métricas permiten explicar claramente al equipo técnico cómo impactan estas variables en el resultado esperado.

## ¿Cómo visualizar y entender las predicciones realizadas?
En la etapa de predicción, se utiliza el método predict para calcular la diferencia de goles esperada en nuevos datos, combinando estas predicciones con valores reales para comparar resultados fácilmente. Además, mediante gráficas de dispersión claras y visuales creadas con matplotlib y seaborn, se comparan resultados reales frente a los predichos:

* Cada punto representa una comparación específica.
* La cercanía entre puntos y línea ideal sugiere la calidad del ajuste.

La interactividad también se incorpora mediante controles deslizantes ('sliders'), permitiendo al entrenador explorar diferentes escenarios según posesión y tiros al arco, para evaluar dinámicamente las predicciones del modelo en tiempo real.