# División de datos en machine learning con train_test_split

## Resumen

## ¿Qué es la capacidad de generalización en machine learning?
Para asegurar que un modelo de machine learning realmente funciona con datos nuevos, es fundamental evaluar su capacidad de generalización. Esto implica verificar si el modelo puede mantener un buen rendimiento con datos nunca antes vistos, evitando la memorización u overfitting en conjuntos de entrenamiento.

## ¿Cómo dividir conjuntos de datos correctamente?
El método recomendado y estándar para verificar la generalización de modelos es dividir el conjunto inicial de datos en dos partes esenciales:

1. **Datos de entrenamiento (train set)**: Utilizados para que el modelo aprenda.
2. **Datos de prueba o validación (test set)**: Sirven para comprobar el desempeño del modelo en nuevos datos.

Habitualmente se utiliza una proporción de 80-20, es decir, el 80% para entrenamiento y el 20% restante para prueba, lo cual ofrece un balance ideal entre aprendizaje y validación.

## ¿Qué es la función train_test_split?
En Python, la función `train_test_split` proveniente de la biblioteca scikit-learn permite dividir los conjuntos de datos de forma eficiente y aleatoria:

```Python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```

Aquí, el parámetro `test_size` determina el tamaño de los datos destinados para pruebas, mientras que `random_state` asegura que los resultados sean reproducibles en diferentes ejecuciones.

## ¿Cómo utilizar widgets interactivos en notebooks?
El uso de widgets interactivos en notebooks facilita la exploración dinámica de cómo afecta variar el tamaño de los conjuntos de datos separando entrenamiento y pruebas. Se implementa de siguiente forma:

```Python
import ipywidgets as widgets
widgets.interactive(dividir_datos, test_size=widgets.FloatSlider(value=0.2, min=0.1, max=0.5, step=0.01))
```

Este slider interactivo permite que se observe en tiempo real cómo diferentes proporciones del conjunto de datos influyen en el rendimiento del modelo, contribuyendo así a mejores decisiones sobre el tamaño ideal del set de prueba.

## ¿Cómo interpretar resultados obtenidos con esta técnica?
Si después de dividir nuestros datos, entrenamos un modelo y obtenemos buenos resultados en el set de prueba, podemos afirmar con confianza que el modelo tiene una buena capacidad para generalizar a situaciones no vistas anteriormente. Esto responde satisfactoriamente a la duda común sobre si el modelo funcionará correctamente frente a nuevos escenarios, perspectivas o contextos.