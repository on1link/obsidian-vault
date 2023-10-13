  * ## Abstract
    * Time series forecasting is an important problem across many domains, including predictions of solar plant energy output, electricity consumption, and traffic jam situation. In this paper, we propose to tackle such forecasting problem with Transformer [1]. Although impressed by its performance in our preliminary study, we found its two major weaknesses: (1) locality-agnostics: the point-wise dot-product self-attention in canonical Transformer architecture is insensitive to local context, which can make the model prone to anomalies in time series; (2) memory bottleneck: space complexity of canonical Transformer grows quadratically with sequence length L, making directly modeling long time series infeasible. In order to solve these two issues, we first propose convolutional self-attention by producing queries and keys with causal convolution so that local context can be better incorporated into attention mechanism. Then, we propose LogSparse Transformer with only O(L(log L)2 ) memory cost, improving forecasting accuracy for time series with fine granularity and strong long-term dependencies under constrained memory budget. Our experiments on both synthetic data and real-world datasets show that it compares favorably to the state-of-the-art.
  * ## Keywords
    * **self-attention, transformer, time series forecasting **
  * ## Relevant Questions & Recall
  * ### Notas
    * Primera pasada
      * [[Roam/Turing/Vaswani, A.2017 Attention is all you need#^roYoHMkd_|Transformer]] was fount two major weakness:
        * 1. *locality-agnostics*: the point-wise dot-product self-attention in canonical Transformer architecture is insensitive to local context., which can make the model prone to anomalies in time series.
        * 2. *memory bottleneck*: space complexity of canonical Transformer grows quadratically with sequence length *L,* making directly modeling long time series infeasible.
      * 1. Categoría: ¿Qué tipo de articulo es éste? ¿Un articulo de medición? ¿Un análisis de un sistema existente? ¿Una descripción de un prototipo de investigación?
        * Es un articulo de análisis de un modelo existente (Transformer) y propuestas para poder aplicarlo en Series de Tiempo
      * 2. Contexto: ¿Con qué otros artículos está relacionado? ¿Qué bases teóricas se usaron para analizar el problema?
        * Esta relacionado con los articulos que analizan o han intentado solucionar los problemas de pronosticos en series de tiempo, AR, ARIMA, RNN, LSTM, GRU, y los problemas de las dependencias a largo plazo. Además se basa en el funcionamiento del Transformer Canonico para realizar los cambios necesarios.
      * 3. Exactitud: ¿Los supuestos parecen ser validos?
        * Falta infomación para revisar los supuestos,
      * 4. Contribuciones: ¿Cuáles son las principales contribuciones del artículo?
        * Aplicar exitosamente la arquitectura Transformer en el pronostico de series de tiempo y realizar extensos experimentos tanto en datasets sinteticos y reales para validar el valor potencial del Transformer en manejar de mejor forma dependencias de largo plazo que los modelos basados en RNN.
        * Proponen un nuevo método de *self-attention,* llamado *convolutional self-attention,* utilizando mecanismos de *causal convolution* para producir las *queries* y  en la capa de *self-attention*. *Query-key*  coincidente consciente del contexto local, e.g. formas, pueden ayudar al modelo a alcanzar un *training loss* más bajo y mejorar más el *accuracy* del pronostico.
        * Proponen un modelo nuevo llamado *LogSparse* Transformer, con solo O(L(log L)^2) complejidad espacial para romper con el cuello de botella de memoria, no solo haciendo el modelamiento de series de tiempo largas de granularidad fina más factible sino también produciendo resultados comparables o mejores con mucho menos uso de memoria, comparado con el Transformer canonico.
      * 5. Claridad: ¿Está bien escrito el documento?
        * Plantea bien el proposito del paper, estudio anterior del Transformer y apuntando sus debilidad, además de generar una propuesta para adaptarlo en Series de tiempo.
    * Segunda pasada
      * Modelos tradicionales de pronostico en series de tiempo, tales como [[State Space Models]] (SSMs) y Autoregresivo (), son diseñados para adaptarse a cada modelo de forma independiente. Además requieren de la experiencia del profesional en seleccionar manualmente la tendencia (((*trend*))), la [[Roam/Turing/Time Series#^COlXptt5O|Estacionalidad (Seasonality)]] y otros componentes.
      * Las Redes Neuronales Recurrentes ([[RNN]]) han sido empleadas para modelar series de tiempo. Sin embargo, las *RNN* son notoriamente difíciles de entrenar, debido al problema de [[Definiciones#^17qg8_qCL|**Vanishing Gradient Problem**]] y Exploding Gradient Problem.
      * Con las variantes incluyendo las [[Roam/Turing/Hochreiter, S.1997 Long short-term memory#^3_jkgVv5j|LSTM]] y [[GRU]] los problemas siguen sin resolver. Por ejemplo la LSTM tiene problemas para capturar dependencias de largo plazo.
      * El *[[Roam/Turing/Vaswani, A.2017 Attention is all you need#^roYoHMkd_|Transformer]]* ha sido propuesto como una nueva arquitectura en la cual aprovecha para procesar datos de secuencias. Este permite al modelo acceder a cualquier parte de la historia de la secuencia sin importar la "distancia".
        * Sin embargo el producto punto canónico de *self-attention* hace coincidir las *queries* con *keys* insensibles al contexto local, el cual como consecuencia el modelo es propenso a anomalías y traer problemas de optimización subyacentes.
        *  Además la complejidad espacial del Transformer canonico crece cuadraticamente con el tamaño de la entrada L.
          * Problemas de cuello de botella en la memora en series de tiempo largas de granularidad fina.
      * Hay muchas aplicaciones para el pronósticos, y varios métodos han sido propuestos para resolver el problema.
        * Uno de los más prominentes es el ARIMA con la [[Metodología Box-Jenkins]] para la selección del modelo.
          *  Sin embargo el supuesto lineal y la limitaciones de escalabilidad lo hacen inadecuado para tareas de pronóstico a gran escala.
          * La información a través de series de tiempo similar no se puede compartir dado que cada series de tiempo es adaptada individualmente.
        * También hay modelos que relacionan los datos de la series como una matriz y resuelven el pronóstico como un problema de factorización matricial
        * Métodos Bayesianos jerárquicos para aprender a través de  múltiples series de tiempo de conteo relacionadas desde la perspectiva del modelo gráfico.
        * Redes Neuronales Profundas se han propuesto para capturar la información compartida a través de series de tiempo relacionadas para un pronóstico más preciso
        * El Transformer basado en *self-attention* para el modelado de secuencias, usado en tareas como, traducción, habla, música y generación de imagenes.
          * Sin embargo, escalar la atención a secuencias extremadamente largas es computacionalmente prohibitivo dado que la complejidad espacial del *self-attention* crece cuadraticamente con el largo de la secuencia. 
          * Un problema para pronosticar series de tiempo con granularidad fina y dependencias a largo plazo fuertes.
      * [ ] **Definición del problema (usar en 2-3 ML)**
        * Suponer que se posee una colección de *N* series de tiempo univariadas relacionadas $$\{\boldsymbol{z}_{i,1:t_0}\}^N_{i=1} $$, donde:
          * $$\boldsymbol{z}_{i,1:t_0} \triangleq [\boldsymbol{z}_{i,1}, \boldsymbol{z}_{i,2}, \cdots, \boldsymbol{z}_{i,t_0}]$$
          * $$ \boldsymbol{z}_{i,t} \in {\rm I\!R}$$ denota el valor de la serie de tiempo $$i$$ en el tiempo $$t$$
        * Vamos a predecir los siguientes $$\tau$$ pasos hacia adelante para todas las series, es decir:
          * $$\{\boldsymbol{z}_{i,t_0+1:t_0 + \tau}\}^N_{i=1}$$
        * Además, suponer que $$\{\boldsymbol{x}_{i,1:t_0+ \tau}\}^N_{i=1} $$ es un conjunto de vectores covariables asociados basados en el tiempo con dimensión $$d$$ que se supone que se conocen durante todo el período de tiempo, e.g. día de la semana y hora del día.
        * El objetivo es modelar la siguiente distribución condicional:
          * $$p(\boldsymbol{z}_{i,t_0+1:t_0+\tau}| \boldsymbol{z}_{i,1:t_0},\boldsymbol{x}_{i,1:t_0+\tau}; \Phi) = \displaystyle\prod^{t_0+\tau}_{t=t_0+1} p(\boldsymbol{z}_{i,t} | \boldsymbol{z}_{i,1:t-1}, \boldsymbol{x}_{i,1:t}; \Phi)$$
        * Se reduce el problema a aprender un modelo de predicción un paso adelante:
          * $$p(z_t|z_{1:t-1},x_{1:t}; \Phi)$$, se omite $$i$$ por simplicidad
          * Donde $$\Phi$$ denota los parámetros aprendibles compartidos por todas las series de tiempo en la colección.
        * Para utilizar tanto las observaciones como las covariables, las concatenamos para obtener una matriz aumentada de la siguiente manera:
          * $$\boldsymbol{y} \triangleq [\boldsymbol{z}_{t-1} \circ \boldsymbol{x}_t] \in {\rm I\!R}^{d+1}$$, donde $$[\cdot \circ \cdot]$$ representa concatenación.
          * $$ \boldsymbol{Y}_t = [\boldsymbol{y}_1, \cdots, \boldsymbol{y}_t]^T \in {\rm I\!R}^{t \times(d+1)}$$
        * Un modelo apropiado $$\boldsymbol{z}_t \sim f(\boldsymbol{Y}_t)$$ es entonces explorado para predecir la distribución de $$\boldsymbol{z}_y$$ dado $$\boldsymbol{Y}_t$$
        * Se instancia $$f$$ con el Transformer.
      * **Se define el Transfomer**_
        * Se puede tomar ventaja del mecanismo de *self-attention* multi-cabezal, ya que éste permite al Transformer capturar ambas dependencias de largo y corto plazo, y cada cabezal aprende a enfocarse en diferentes aspectos de los patrones temporales.
        * Transforman la matriz $$\boldsymbol{Y}$$ en *H* matrices $$\boldsymbol{Q}_h = \boldsymbol{YW}_{h}^{Q}$$, $$ \boldsymbol{K}_h  = \boldsymbol{YW}_{h}^{K}, $$ $$ \boldsymbol{V}_h =  \boldsymbol{YW}_{h}^{V}$$$
        * En la softmax del mecanismo de atención se le aplica una matriz de mascara $$\boldsymbol{M}$$ para filtrar la atención hacia la derecha, para evitar fuga de información futura.
      * **Mejorando la localidad del Transformer**
        * Los patrones de las series de tiempo pueden evolucionar con el tiempo dado a varios eventos, entonces, si un punto observado es una anomalía, el punto de cambio o parte de los patrones depende en gran medida de su contexto que lo rodea.
        * Sin embargo en las capas de *self-attention* las similaridades entre las *queries* y las *keys* son calculadas basadas en sus valores puntuales sin aprovechar completamente el contexto local como la "forma".
        * La coincidencia de la *query-key* agnóstica del contexto local puede confundir al modulo de *self-attention* en términos de donde el valor observado es una anomalía, un punto de cambio o parte de los patrones, y llegar a problemas de optimización subyacentes.
        * ***Self-attention* convolucional**
          * En vez de ocupar una convolución con tamaño de kernel 1 y con stride 1 paso (multiplicación de matriz), se emplea una *convolución causal* con tamaño de kernel *k* y con stride 1 para transformar las entradas (con el apropiado padding) en *queries* y *keys*. Como consecuencia se tiene un más conciencia del contexto local y calcular las similadirdad usando información local, e.g. "formas" en lugar de valores puntuales.
          * Notar que la *Convolución causal * se asegura que la posición actual nunca tenga acceso a información futura.
          * Con $$k=1$$, la *self-attention* convolucional se degrada al *self-attention* canonico, entonces ésta es una generalización
          * ![[Roam/Turing/Attachments/imgs/app/Turing/qcou_XFrVl.png]]
        * **Rompiendo el cuello de botella de memora en el Transformer**
          * Se realizo una evaluación cualitativa de los patrones de atención aprendidos con un Transformer canónico, con *full attention* y se visualizaron los patrones de atención aprendidos.
          * En los resultados en algunas capas de atención (capas), solo se exhibió un *sparsity* dependiente del patrón. lo que sugiera que alguna forma de *sparsity* puede ser introducida sin afectar el rendimiento de forma significativa.
          * Para una secuencia de largo $$L$$, calcular las puntuaciones de atención entre cada par de celdas causa un uso de memoria del orden $$O(L^2)$$, haciendo que el modelamiento de series de tiempo largas con granularidad fina y dependencias de largo plazo fuerte prohibitivo.
          * ***LogSparse* Transformer**
            * Solo necesita calcular $$O(log L)$$ productos puntos para cada celda en cada capa.
            * Solo se necesita apilar hasta $$ O(log L)$$ capas y el modelo será capaz de acceder a la información de cada celda.
            * Entonces el costo total de uso de memoria es solo $$O(L(logL)^2)$$
            * [ ] Escribir la definicion de como cada celda presta atención $$I$$
            * ![[Roam/Turing/Attachments/imgs/app/Turing/GT7iSCv_u-.png]]
            * *LogSparse* self-attention permite a cada celda solo tomar atención a sus celdas previas con un tamaño de paso exponencial y a si misma.
              * $$ \forall k$$ y $$l$$, $$I^k_l = \{l - 2^{[log_2 l]}, l - 2^{[log_2 l]-1}, l - 2^{[log_2 l]-2}, \ldots, l - 2^{0}, l\}$$
              * $$[\cdot]$$ Denota la operación piso como muestra la figura(b):
              * ![[Roam/Turing/Attachments/imgs/app/Turing/Dc4t3WtnSm.png]]
            * **Local Attention**
              * Se permite a cada celda a prestar atención de manera densa a las celdas en su ventana izquierda de tamaño $$O(log_2 L) así más información local, e.g. tendencia, puede ser aprovechada en el paso actual del pronostico.
              * Más allá de las celdas vecinas, se resume la estrategia de atención *LogSparse*.
              * ![[Roam/Turing/Attachments/imgs/app/Turing/67kTRKY4J5.png]]
            * **Restart Attention**
              * Se puede dividir toda la entrada de tamaño $$L$$ en sub-secuencias y cada una de largo $$L_{sub} \propto L $$. Para cada sub-secuencia, se aplica la estrategia de atención *LogSparse*.
              * ![[Roam/Turing/Attachments/imgs/app/Turing/HPuQVZH-6p.png]]
      * [ ] **Experimentos**
      * **Trabajo futuro**
        * Explorar mejores estrategias de *sparsity* en la *self-attention* y extender el método para que modele mejor datasets pequeños.
  * ## References
    * [[Vaswani, A.2017 Attention is all you need]]
    * [[Pascanu, R., Mikolov, T., Bengio, Y.2013 On the difficulty of training recurrent neural networks]]
    * Durbin:2012 "Time series analysis by state space methods"
    * Graves:2013 "Generating sequences with recurrent neural networks"
    * Sutskever:2014 "Sequence to sequence learning with neural networks"
    * Lai:2018 "Modeling long-and short-term temporal patterns with deep neural network".
    * [[Hochreiter, S.1997 Long short-term memory]]
    * Cho:2014 "On the properties of neural machine translation: Encoder-decoder approaches"
    * Box;Jenkings:1968 "Some recent advances in forecasting and control"
    * Box;Jenkins:2015 "Time series analysis: forecasing and control"
    * Yu:2016 "Temporal regularized matrix factorization for high-dimensional time series prediction"
    * [[Huang;Vaswani2018 An improved relative self-attention mechanism  for transformer with application to music generation]]
    * Povey:2018 "A time-restricted self-attention layer for asr"
    * Poggio:2017 "Why and when can deep-but no shallow-networks avoid the curse of dimensionaltiy: a review"
    * Borovykh:2017 "Conditional time seies forecasting with convolutional neural networks"
    * Yu:2017 "Deep learning: A generic approach for extreme condition traffic forecasting"
    * [[Zhang1998 Forecasting with artificial neural networks The state of the art]]
    * [[Child, R2019 Generating long sequences with sparse transformers]]
    * Laptev:2017 "Time-series extreme event forecasting with neural networks at uber"