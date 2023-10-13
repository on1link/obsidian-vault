  * **Esta clase de métodos intenta evitar el sobreajuste (*overfitting*) durante el entrenamiento**
  * En general estas técnicas modifican el entrenamiento de las siguientes formas:
    * Penalizando la complejidad del modelo, para que la red decida implementar funciones más complejas solo si lo vale o es necesario.
      * Regularización L1; Regresión Lasso
      * Regularización L2; Regresión Ridge
      * NOTA: En ocasiones lo ocupan para [[Roam/Turing/Selección/Extracción de características|Selección/Extracción de características]] y así reducir la dimensionalidad de los datos
    * Reduciendo la varianza de la estimación, esto es, incrementando la robustez del modelo frente a variaciones en el conjunto de entrenamiento.
    * Codificar un a-priori (información del dominio del problema) en cual tendría que ser el modelo óptimo.