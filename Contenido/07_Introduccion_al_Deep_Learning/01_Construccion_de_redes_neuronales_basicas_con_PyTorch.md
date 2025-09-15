# Construcción de redes neuronales básicas con PyTorch

## Resumen

Las redes neuronales artificiales (RNA) son fundamentales en el área del deep learning y permiten avances en diversos proyectos de inteligencia artificial. Estas redes aprenden de forma autónoma mediante datos, realizando tareas complejas como clasificaciones binarias. Utilizando PyTorch, conoceremos cómo funciona una RNA sencilla partiendo desde cero hasta evaluar sus resultados.

## ¿Qué herramientas necesitas para construir una RNA?
Para iniciar con redes neuronales, necesitas herramientas que faciliten su construcción. PyTorch es una biblioteca esencial para definir estructuras neuronales, específicamente sus módulos:

* **Torch**: para trabajar con tensores y cálculos automáticos de gradientes (autograd).
* **Torch.nn**: contiene módulos para configurar capas neuronales como lineales.
* **Torch.optim**: gestiona la actualización automática de pesos durante el entrenamiento.
* **NumPy**: indispensable para manipular datos como arrays.

Con estas herramientas, creamos un entorno práctico y efectivo para modelar soluciones con inteligencia artificial.

## ¿Cómo se crea y entrena una red neuronal sencilla?
Crear una RNA comienza generando un conjunto de datos sintéticos, por ejemplo, 100 muestras con cuatro características y etiquetas binarias. Luego se convierten estos datos en tensores con PyTorch para entrenar la red.

La arquitectura básica empleada incluye:

* Una capa oculta con activación ReLU de 8 neuronas,
* Una capa final activa con función sigmoide para realizar clasificación binaria.

Durante el entrenamiento definimos la pérdida con `BCELoss` que trabaja con salidas entre 0 y 1. Utilizamos el optimizador `Adam`, que ajusta los pesos según los gradientes calculados automáticamente.

El entrenamiento completo comprende varias épocas donde se calculan las predicciones, pérdida, actualización de pesos y la respectiva precisión obtenida.

## ¿Cómo puedes evaluar el rendimiento y mejorar tu RNA?
La evaluación precisa del rendimiento consiste en transformar las probabilidades en etiquetas binarias utilizando un umbral de 0.5, comparando con las verdaderas etiquetas para medir el porcentaje de aciertos.

Además, puedes inspeccionar rápidamente la estructura total de la red visualizando:

* Información detallada de cada capa.
* Cantidad y dimensiones de los parámetros entrenables.

Finalmente, mediante una interfaz interactiva, cambiando fácilmente la profundidad (cantidad de capas ocultas), puedes observar cómo afecta la precisión del modelo. Esto permite entender claramente el equilibrio entre capacidad del modelo y riesgo de sobreajuste.