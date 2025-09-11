# Creación de variables predictivas en machine learning

## Resumen

¿Alguna vez has escuchado sobre la ingeniería de características o feature engineering? Si trabajas con machine learning o quieres optimizar tus predicciones, saber crear nuevas variables es fundamental. Básicamente, la ingeniería de características consiste en transformar datos crudos en información más relevante para los modelos, ayudándolos a descubrir patrones más profundos y efectivos.

## ¿Qué es exactamente la ingeniería de características?
La ingeniería de características implica generar nuevas variables a partir de las existentes. Al hacerlo, los algoritmos pueden captar mejor lo que sucede realmente con nuestros datos. Por ejemplo, en un análisis futbolístico, en lugar de usar únicamente los goles marcados por separado, podemos crear variables como:

* Diferencia de goles: goles locales menos goles visitantes.
* Ratio de tiros sobre posesión local: tiros al arco locales sobre posesión local.

Estas nuevas variables aportan mayor contexto y permiten modelos más precisos.

## ¿Cómo crear nuevas variables claves en nuestro dataset?
En este caso práctico, utilizamos Python y la librería `pandas` para crear nuevas variables útiles en nuestro proyecto futbolístico.

### Diferencia de goles como variable objetivo
Esta variable, calculada de la siguiente forma:

```Python
df['diferencia_goles'] = df['goles_local'] - df['goles_visitante']
```

permite determinar claramente si el equipo ganó, empató o perdió.

### Ratio de tiros sobre posesión local
Creamos esta otra nueva característica clave usando esta fórmula:

```Python
df['ratio_tiros_posesion_local'] = df['tiros_arco_local'] / df['posesion_local']
```

Este dato revela cuánto aprovecha realmente el equipo la posesión para generar oportunidades.

## ¿Por qué estas variables ayudan tanto a mejorar las predicciones?
Los modelos basados en algoritmos no identifican automáticamente relaciones profundas y contextuales. La creación de estas nuevas variables proporciona a nuestros modelos la capacidad de identificar patrones valiosos al entregarles información procesada más significativa. Una sola nueva variable, como la diferencia de goles, puede ofrecer mejoras significativas, superiores incluso a cambiar el algoritmo utilizado.

## Visualización y análisis posterior
Más allá de simplemente crear nuevas variables, se necesitan visualizar y analizar para evaluar su eficacia. En el proyecto, realizamos estas dos acciones clave:

* **Histograma muestra la distribución de la diferencia de goles** y nos indica rápidamente cómo tiende a desenvolverse nuestro equipo en los partidos.
* **Mapa de calor (correlación)**: calcula y presenta visualmente la correlación entre las variables originales y las nuevas creadas, detectando relaciones lineales útiles.

Por ejemplo, la diferencia de goles mostró una correlación destacada con los goles de local, alcanzando un valor de 0.7, indicando que es una variable sumamente informativa.