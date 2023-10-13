  * # Abstract
    * Wind speed forecasting is crucial for the penetration of wind energy sources in electrical systems, since accurate wind speed forecasts directly translates into accurate wind power predictions. A framework called Multi-scale RNNs specifically addresses the issue of learning long term dependencies in RNNs. Following that approach, we devised a LSTM-based Multi-scale model that learns to build different temporal scales from the original wind speed series that are then used as input for multiple LSTMs, whose final internal states are used to forecast wind speed future values. Results from two real wind speed datasets from northern Chile show that this approach outperforms the standard LSTM and its capable of working with very long input series without overfitting, while being computationally efficient regarding training times.
  * ## Notas
    * ## Primera pasada
      * **1. Categoría:** ¿Qué tipo de articulo es éste? ¿Un articulo de medición? ¿Un análisis de un sistema existente? ¿Una descripción de un prototipo de investigación?
        * Un análisis de un problema existente en las RNN y LSTM en cuanto al procesamiento de series de entrada largas, y un prototipo de investigación para Wind Forecasting.
      * **2. Contexto**: ¿Con qué otros artículos está relacionado? ¿Qué bases teóricas se usaron para analizar el problema?
        * Primer artículo; Señala la dificultad de pronosticar velocidad de viento debido a su naturaleza. Dentro de todas las técnicas usadas en la literatura, se enfoca en las RNN debido a su capacidad natural de modelar dinámicas temporales complejas (que se puede en contrae en procesos naturales tales como el viento); y buen desempeño para Wind Forecasting superando a ARIMA. Exponiendo las debilidades tanto de la RNN y como la LSTM, el autor se basa en una clase de modelos de las RNN llamado Multi-scale RNNs para mitigar el problemas en el aprendizaje de secuencias largas.
      * 3. **Exactitud** (*correctness*): ¿Los supuestos parecen ser validos?
        * EL combinar modelos de redes neuronales basándose en una clase jerárquica para resolver el problema de aprender secuencias muy largas de las LSTM y RNN por si solas. Dudas de como resuelve el costo computacional extra en el entramiento.
      * 4. **Contribuciones:** ¿Cuáles son las principales contribuciones del artículo?
        * Un nuevo modelo que aprende a construir distintas escalas temporales de la serie original de velocidad de viento que son usadas para como entrada para múltiples LSTM, cuyos estados internos finales son usados para pronosticar valores de velocidad de viento futuros.
          * Tener mejor rendimiento que una LSTM para el problema de wind speed forecasting.
          * Ser capaz de aprender series de entrada largas sin sufrir de sobreajuste (*overfitting*) mientras es computacionalmente eficiente con respecto a los tiempos de entrenamiento.
      * 5. **Claridad:** ¿Está bien escrito el documento?
        * Introducción clara, marco teórico explica bases de propuesta RNN, LSTM, Multi-scale RNN, propuesta, experimentos y resultados.
    * ## Segunda pasada
      * Las RNNs tienen mejor rendimiento que los modelos ARIMA en la tarea de pronostico de viento.
      * También se ha aplicado con exito un enfoque hibrido en el cual la serie original se descompone en multiples sub-series para entrenar las RNNs mejorando su capacidad de **generalización**.
      * Las RNN debido a su arquitectura tienen un problema importante; el aprendizaje de relaciones temporales a largo plazo en los datos usando back-propagation es difícil debido al problema de **Gradiente Desvaneciente ([[Roam/Turing/Definiciones#^17qg8_qCL|**Vanishing Gradient Problem** ^17qg8_qCL]]).**
      * Una RNN usada para este problema es la LSTM, cuyos nodos internos son bloques de memoria que pueden prevenir que el gradiente se desvanezca a través de su Constant Error Carousel, sin embargo dependencias de muy largo plazo aún es imposible de aprender usando solo este enfoque.
      * En la comunidad de wind speed forecasting, aunque usar la LSTM es la red recurrente de elección, este problema aún no se ha abordado directamente .
      * De las RNNs, después de procesar una serie, los estados internos finales pueden ser usados para calcular la salida de la red (network), la cual en la tarea de pronostico podría ser el valor pronosticado 1 paso adelante.
      * ### Multi-scale RNN
        *  La idea detrás de esta estructura es ayudar al modelo a aprender dependencias a largo plazo (long-term dependencies; ojo no es lo mismo que una secuencia larga). Los nodos de baja frecuencia son menos propensos a olvidar información del pasado a medida que llega nueva información. Los nodos en estas redes son agrupados en jerarquías, haciendo a éstas más capaces de aprender relaciones a largo plazo complejas y estructuras temporales jerarquicas en los datos.
        * Una caracteristica de las redes ya diseñadas es que realizan predicciones basadas en la última capa de la jerarquía. Otras capaz individuales pueden contener información relevante de su escala, que puede ser dificil de recuperar si solo la última capa es tomada en cuenta para calcular el pronóstico.
        * La propuesta LSTM-MultiScale desacopla el mechanismo de construcción de escalado (usando FFN para construir multiples subseries que aliementan las LSTMs), se puede controlar la cantidad de entradas que cada LSTM recibe y así evitar incrementos excesivos en los costos computacionales al añadir más escalas (de tiempo) al modelo.
        * Cada sub-serie creada mediante una FFN será considerada como una escala. Dado que cada sub-serie es construida desde multiple valores de una previa, su largo va disminiyendo. Cada escala entonces tiene caracteristicas especificas que pueden ser útiles:
          * $$ y= w^T s $$
        * ![image](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ff1b2ccf-d5da-42fc-9270-ec4e3ecfa758/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAT73L2G45O3KS52Y5%2F20200502%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20200502T222742Z&X-Amz-Expires=86400&X-Amz-Signature=a40d390ca0d0ec73b5a9198801ca03fa39934596fa13f583e23d822bc5edadf2&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22)
        * El objetivo es pronosticar la velocidad de viento de 1 a 24 horas después de la última observación medida.
        * Para producir el valor de salida, cada estado interno final de todas las LSTMs son concatenadas para producir un vector final, del cual la salida de la red es calculada mediante una simple combinación lineal de sus valores.
        * ** El dataset de la serie son dos torres de prospeccción con 25719 y 19536 datos; Se crearon 10 sub-series aplicando una ventana deslizante creando una diferencia de 30% entre sub-series consecutivas. Cada sub-serie contiene 6950 y 5279 mediciones por hora consecutiva respectivamente. Cada sub-serie normalizada en el rango [0, 1].
        * De baseline se ocupa un modelo persistente *ingenuo* repitiendo los últimos 24 valores.
        * El modelos fue comparado contra una LSTM estándar con múltiples capas apiladas.
        * El pronostico se realizo un paso adelante (hora); mejores resultados en escala 24, 48 (diaria, 2 días) y 24 (diaría) para ambos datasets; El añadir más escalas no incremento de manera significativa el costo computacional al calcular el gradiente per lag, lo que lo hace eficiente, en comparación al añadir capas a la LSTM stacked
    * ## Tercera pasada
  * ## Referencias
    * **Wind Speed**
      * [[Barbounis, T2006b Long-term wind speed and power forecasting using local recurrent neural network models]]
      * [[Liu, H2018 Wind speed forecasting method based on deep learning strategy using empirical wavelet transform, long short term memory neural network and Elman neural network]]
      * [[Liu, H2015 Wind speed forecasting approach using secondary decomposition algorithm and elman neural networks]]
      * [[Cao, Q.2012 Forecasting wind speed with recurrent neural networks]]
      * [[Wang, J.2014 Forecasting wind speed using empirical mode decomposition and Elman neural network]]
    * **Time Series**
      * Hallas, M., Dorffner, G.: A comparative study on feedforward and recurrent neural networks in time series prediction using gradient descent learning (1998)
    * **LSTM**
      * [[Hochreiter, S.1997 Long short-term memory]]
    * **RNN**
    * [[Pascanu, R., Mikolov, T., Bengio, Y.2013 On the difficulty of training recurrent neural networks]]
    * **Multi-Scale RNN:**
      * Koutnik, J., Greff, K., Gomez, F., Schmidhuber, J.: A clockwork RNN. In: International Conference on Machine Learning, pp. 1863–1871, January 2014
      * Chung, J., Ahn, S., Bengio, Y.: Hierarchical multiscale recurrent neural networks. arXiv preprint arXiv:1609.01704 (2016)