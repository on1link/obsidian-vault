  * Un problema subyacente cuando intentamos crear un mapeo entre las entradas y las salidas es saber si las características de las entradas son relevantes para el modelo
  * Podemos aplicar selección de características para reducir el número de características.
  * Por lo que se necesita un procedimiento de búsqueda heurística para encontrar un buen subconjunto de características
  * **Métodos Wrapper**
    * Generan modelos *wrapper* debido a que es un procedimiento que se envuelve alrededor del algoritmo de aprendizaje, haciendo diferentes llamadas al algoritmo de aprendizaje para evaluar que tan buen rendimiento se tiene con diferentes subconjuntos de características
    * **Foward Selection**
    * **Backward Selection**
  * **Métodos de Filtro**
    * Heurísticas para realizar de manera más barata la selección de características.
    * Se calcula un puntaje simple que mide que informativa es una característica $X^{(i)}$ sobre sus etiquetas ($y$).
    * Se eligen los $K$ mejores puntajes, pareciendo de manera natural seleccionar las características que más se correlacionan.
    * **Información Mutua** es uno de los puntajes más populares
  * **[[PCA]]**
    * Es una técnica para obtener un conjunto reducido de proyecciones lineales ortogonales de una colección de variables correlacionadas.
    * Puede ser usada como una técnica de reducción de dimensionalidad.
  * **Extracción de características para clasificación**
    * **Discriminador lineal de Fisher**
