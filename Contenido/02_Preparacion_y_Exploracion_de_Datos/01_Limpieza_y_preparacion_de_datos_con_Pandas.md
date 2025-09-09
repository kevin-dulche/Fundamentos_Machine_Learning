# Limpieza y preparación de datos deportivos con Pandas

## Resumen

Transformar datos brutos en conocimientos útiles es crucial para cualquier tipo de análisis. En este proceso, utilizar Python y la librería Pandas facilita organizar y preparar información, incluso cuando los datos iniciales son incompletos o poco claros. Explorar este camino permite identificar errores, duplicados, y convertir variables sin complicaciones, construyendo una base sólida lista para futuros análisis predictivos.

## ¿Por qué importar los datos usando Pandas?
La librería Pandas es una herramienta poderosa y eficiente para manipular grandes volúmenes de datos. Al realizar la importación, la función `read_csv` permite cargar archivos CSV, mientras que la función `head` ofrece una muestra inicial para confirmar que la información se haya cargado correctamente.

```Python
import pandas as pd

datos_ceballitas = pd.read_csv("partido_cebollitas.csv")
print(datos_ceballitas.head())
```

Este paso facilita una primera aproximación, permitiendo visualizar las cinco primeras filas del dataset más claramente.

## ¿Cómo detectar y tratar datos faltantes?
Al verificar la presencia de valores nulos, es posible determinar si los datos requieren acciones correctivas. Utilizando la combinación de métodos como `isnull()` y `sum()`, podemos afirmar si existe ausencia de información en alguna columna específica:

```Python
print(datos_ceballitas.isnull().sum())
```

Si aparecen datos faltantes, una técnica común es imputar valores promedio en lugar de eliminar registros, especialmente importante para no descartar información útil.

## ¿Cuándo y por qué codificar variables categóricas?
Para llevar a cabo modelos predictivos, los nombres de equipos deportivos, clasificados como variables categóricas, deben convertirse en formato numérico. La función `get_dummies()` transforma estas categorías en columnas binarias, utilizando unos y ceros para indicar la presencia o ausencia de una categoría específica:

```Python
datos_preparados = pd.get_dummies(datos_ceballitas, columns=["equipo_local", "equipo_visitante"])
```

Este método es claro y facilita la interpretación de datos por parte de algoritmos automáticos.

## ¿Vale la pena identificar y eliminar duplicados?
Los registros duplicados pueden distorsionar cualquier modelo predictivo. La función `duplicated()` es útil para detectar y remover duplicados automáticamente:

```Python
datos_preparados = datos_preparados.drop_duplicates()
```

Este paso asegura que la información contenida en el dataset sea única y no confunda al proceso de aprendizaje automático.

## ¿Cómo convertir columnas de fechas en un formato adecuado?
El análisis temporal de los datos requiere un formato adecuado de fechas. La función `to_datetime()` transforma cadenas en objetos de tiempo reconocibles por Python y Pandas, facilitando futuros análisis:

```Python
datos_ceballitas["fecha"] = pd.to_datetime(datos_ceballitas["fecha"], errors='coerce')
```

El parámetro `errors='coerce'` es útil para manejar fechas inválidas, marcándolas claramente para tomar acciones consistentes.

## ¿Qué información adicional revisamos al final?
Tras la limpieza y preparación, es recomendable obtener un resumen completo con el método `info()`, que incluye:

* Número y tipo de columnas.
* Presencia de datos nulos.
* Memoria utilizada por el dataset.

```Python
print(datos_preparados.info()) 
print(datos_preparados.info(memory_usage='deep')) # Uso de memoria completo
```

Al verificar que no queden valores faltantes y contabilizar columnas finales, se garantiza la calidad de los datos antes de iniciar cualquier análisis predictivo.
