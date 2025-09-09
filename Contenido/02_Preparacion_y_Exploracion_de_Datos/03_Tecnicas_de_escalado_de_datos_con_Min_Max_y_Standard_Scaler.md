# Técnicas de escalado de datos con Min Max y Standard Scaler

## Resumen

Cuando trabajamos con modelos predictivos, contar con datos en escalas diferentes puede afectar significativamente su precisión. Variables con rangos distintos, como la posesión del balón representada en porcentaje y los tiros al arco contabilizados en números absolutos, tienden a confundir a los algoritmos. Esto suele ocurrir porque los modelos interpretan magnitudes mayores como más relevantes, aunque no necesariamente lo sean. Por ello, es clave aplicar técnicas que igualen las escalas de nuestros datos.

## ¿Por qué escalar los datos antes del entrenamiento?
Escalar datos permite normalizar y centrar variables, facilitando que nuestros algoritmos aprendan sin sesgos derivados de la magnitud numérica. Pensemos en un ejemplo práctico: un delantero con doce tiros al arco frente a una posesión de equipo del cincuenta y cinco por ciento. Si no ajustamos las escalas, el modelo podría interpretar incorrectamente mayor relevancia en los doce tiros por valor absoluto más alto.

Estos ajustes pueden realizarse con dos técnicas clave:

* **Min Max Scaling (Normalización)**: transforma valores a un rango uniforme (habitualmente entre cero y uno).
* **Standard Scaler (Estandarización)**: reescala variables para tener una media de cero y desviación estándar de uno.

## ¿Cómo aplicamos Min Max Scaling (normalización)?
Esta técnica es ideal cuando los datos no siguen distribuciones normales y permite transformar variables a un rango fijo entre cero y uno. Por ejemplo, con los tiros al arco de un jugador:

* Si el jugador realiza doce tiros de un máximo registrado de quince, se obtiene un resultado normalizado de 0.8.

Pasos para su implementación básica:

1. Crear una instancia de MinMaxScaler.
2. Utilizar el método `.fit_transform()` para calcular y aplicar la normalización rápidamente.
3. Incorporar los resultados normalizados en nuevas columnas para análisis posteriores.

## ¿Cuándo usar Standard Scaler (estandarización)?
Si buscas mantener la distribución original de tus datos, opta por la estandarización. Esta técnica centrará y ajustará los datos para que su media sea cero y su desviación estándar sea de uno. Resulta especialmente útil para algoritmos sensibles a la escala, como la regresión o PCA.

Pasos claros al emplear este método:

1. Crear una instancia de StandardScaler.
2. Aplicar nuevamente `.fit_transform()` para obtener datos centrados y estandarizados.
3. Guardar resultados en columnas específicas, asegurando la consistencia en el análisis.

## Visualización de resultados tras el escalamiento
Para verificar efectivamente el impacto del escalado, resulta útil emplear histogramas. Estas visualizaciones permiten identificar claramente si hemos logrado nivelar o centralizar nuestras variables.

El proceso recomendado incluye:

* Utilizar Matplotlib y Seaborn para generar visualizaciones claras y atractivas.
* Observa cómo se distribuyen tus datos normalizados y estandarizados mediante histogramas paralelos.
* Aprovechar las gráficas para identificar patrones o sesgos residuales.

Tras la aplicación de estas técnicas, contamos con datos que garantizan mejores rendimientos y mayores seguridades en las predicciones realizadas por los modelos. Ahora, cada variable aportará equitativamente, independientemente de sus diferencias originales en escala.