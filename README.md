## Reducción de Dimensiones con SVD y Visualización con t-SNE

Este proyecto utiliza el popular dataset **20 Newsgroups**, un conjunto de correos electrónicos clasificados en 20 categorías temáticas (como ciencia, tecnología, sociedad, entre otros), ampliamente usado en el campo de Procesamiento de Lenguaje Natural (NLP).

### Objetivo
Reducir la alta dimensionalidad de los datos textuales (5000 dimensiones tras aplicar TF-IDF) para facilitar su análisis y visualización.

### Proceso
1. **Carga del dataset:** Se cargan todos los textos y sus etiquetas correspondientes.
2. **Vectorización con TF-IDF:** Se convierte cada documento a un vector numérico, limitando a las 5000 palabras más representativas.
3. **Visualización inicial:** Se aplica t-SNE directamente sobre los vectores TF-IDF para observar cómo se distribuyen los temas (documentos) sin reducir la dimensionalidad.
4. **Reducción con Truncated SVD:** Se reduce la dimensionalidad de 5000 a 100 características principales.
5. **Visualización final con t-SNE:** Se visualizan los datos reducidos en 2D, donde es más fácil interpretar la separación temática entre documentos.

### Resultado
Se observa una mejor separación de las categorías cuando se utiliza **SVD antes de t-SNE**, ya que se eliminan el ruido y la redundancia, manteniendo las características más importantes del texto.

Este enfoque permite entender de forma visual cómo los temas están organizados y separados entre sí, siendo útil para análisis exploratorio de texto y clasificación.
