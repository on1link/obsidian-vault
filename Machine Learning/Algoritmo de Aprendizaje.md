  * **Definiciones**
    * Sea $X$ el espacio de características, e $Y$ el espacio de salida.
    * Nuestra meta es tener un mapeo $f: X \rightarrow Y$, llamada comunmente la **hipótesis** o ***learner*** con $X \subseteq R^n$,  $y \in Y \subseteq R$.
    * Sea $S$ el espacio que abarca las posibles muestras, traídas desde una distribución desconocida $P(\boldsymbol{x}, y)$.
    * Un **Algoritmo de aprendizaje** es el mapeo desde el espacio de conjuntos de entrenamiento al espacio de hipótesis $H$ de posibles soluciones funcionales: $$A: S\rightarrow H \\ S_M \rightarrow A(S_M) = f$$
  * **Capacidad de generalización**
    * Un desafío principal es construir un algoritmo o método automático capaz de estimar ejemplos futuros basado en los fenómenos observados en el conjunto de entrenamiento.
  * **Overfitting**
    * Los algoritmos que memorizan los ejemplos de entrenamiento pero tienen un rendimiento predictivo pobre con ejemplos desconocidos, éste problema se llama sobreajuste o *overfitting*.
  * **Curse of dimensionality**
    * **Maldición de la dimensionalidad** ()
      * En aplicaciones reales de aprendizaje automático, tenemos que lidiar con espacios de entrada de alta dimensionalidad que comprende muchas variables de entrada.
