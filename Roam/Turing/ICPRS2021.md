  * # Motivación
    * ## Rápidez del viento
      * **El desarrollo industrial y el aumento de la población han incrementado la demanda de energía a nivel global**. [Lawan]
      * **El cambio climatico causa graves impactos en la atmósfera tales como tormentas violentas, inundaciones, incendios, ciclones, lluvia ácida y sequías prolongadas.** [Freitas]
      * **Naciones del mundo entero han estado luchando por lograr un desarrollo sustentable a través de la generación de energía desde recursos renovables: sol, viento, agua, biomasa.**  [Freitas]
      * La energía eólica es una de las fuentes de energía renovable de más rápido crecimiento, considerada como una alternativa atractiva a la energía convencional generada desde los combustibles fósiles [Jung] 
      * **La energía eólica es prometedora y ha emergido como una de las energías renovables más seguras, limpias y de crecimiento más rápido en los últimos años.** [Lawan]
      * El viento es un recurso natural, intermitente, incierto y difícil de controlar.[Freitas]
      * **Las ventajas de la energía eólica sobre otras fuentes renovables **[Freitas]:
        * **El viento es una recurso inagotable**
        * **Al contrario de los sistemas solares, las granjas de viento producen energía día y noche.**
        * **Las granjas de viento significan un aumento de la oferta de empleo en regiones económicamente desfavorables**
        * **La generación de viento no produce desechos contaminantes para el medio-ambiente.**
        * **Las granjas de viento tienen ventajas económicas sobre otros sistemas de generación de energía a gran escala.**
        * **El energía eólica tiene un costo-beneficio social y medio-ambiental alto, como también un ciclo de construcción corto, bajo mantenimiento y flexibilidad a la inversión**.
      * **El cuello de botella de este tipo de energía es la variabilidad, la naturaleza estocástica, impredecible y compleja de la rapidez del viento. [Lawan]**
      * El dilema de este tipo de energía es la intermitencia y la naturaleza estocástica de la rapidez del viento. [Lawan]
      * Es de suma importancia predecir con precisión la rapidez del viento, con errores mínimos aceptados para la seguridad y la economía de la utilización de la energía eólica.  [Lawan]
      * La energía eólica creció bruscamente debido a sus ventajas para la generación de energía a gran escala. [Freitas]
      * El pronostico de rapidez del viento consistente es relevante, para evitar perdidas económicas, facilitar la regulación de los sistemas de viento, y incrementar la eficiencia operacional a través de una toma de decisiones más confiable [Freitas]
      * Hay muchos factores que influencian los vientos. Por esto el pronostico de la rapidez del viento es uno de los problemas de investigación más relevantes y desafiantes en el mundo hoy en día [Freitas]
      * La demanda de energía esta rápidamente aumentando debido al crecimiento de la población, la urbanización y la evolución industrial. [Freitas]
      * Las energías renovables son las alternativas más prometedoras para la generación de energía, en donde los combustibles fósiles causan graves impactos medioambientales: incremento de gases invernadero, lluvia ácida, contaminación urbana, derrames de petroleo, y deterioro de la biodiversidad. [Freitas]
      * La diversificación de la producción de la energía puede proveer tarifas más baratas y energía limpia de mejor calidad para la población, y también evita la dependencia en una sola fuente de energía. [Freitas]
      * Para el operador de mercado, el pronóstico de la producción de energía eólica total en un región es más necesaria que el pronóstico de una planta eólica individual.
      * Para el planificador del sistema, es esencial para planificar la instalación de nuevas turbinas eólicas.
      * **Una alta penetración de la energía eólica proporciona un número de desafíos en las operaciones y planificación del sistema eléctrico, debido a la naturaleza incierta y intermitente.** [Jung]
      * En los sistemas de electricidad el suministro de energía debe ser igual a la energía demandada todo el tiempo. La variación en la salida de energía eólica hace que sea difícil mantener este equilibrio. [Jung]
      * La gran desventaja es la intermitencia y la imprevisibilidad. los sistemas eléctricos robustos demanda información relevante para un suministro seguro de electricidad. La falta de resultados consistentes es un problema importante en las granjas de viento [Freitas]
      * **Hay dos enfoques para la predicción de energía[Freitas]:**
        * **Predicción directa de la salida de una turbina de viento**
        * **Predicción indirecta en el cual el pronostico de la rapidez del viento es realizada y entonces convertida en electricidad**
      * **La predicción indirecta es más relevante y popular:**
        * **Granjas de viento vecinas con diferencias modelos de turbinas pueden compartir la misma rapidez del viento**
        * **El pronostico de la rapidez del viento es generalmente más preciso que la predicción directa de energía debido a la mayor correlación espacial del viento**
        * **Es bien sabido que existe una relación no lineal entre la rapidez del viento y la energía de salida de las turbinas de viento.  Una pequeña desviación de la rapidez del viento llevará a un gran error de salida de los sistemas de conducción de viento**.[Lawan]

      * La  energía eólica ha sido reconocida como una alternativa prometedora, fuente de energía limpia comparada a la electricidad  generada por combustibles fósiles. [Deng]
      * **La energía eólica por naturaleza se encuentra que es aleatoria e instantánea en rendimiento, y dependiente de la estación al corto plazo. Para una operación segura de los molinos de viento y de la distribución de la electricidad generada por la energía eólica, es importante pronosticar con precisión la velocidad del viento. **[Deng]
      * Pronosticar de manera precisa la velocidad del viento, especialmente en el corto plazo, sigue siendo un gran desafío. [Deng]
      * **Herramientas de pronósticos precisas reducen los costos operacionales y mejoran la fiabilidad asociada con la integración de la energía eólica en el sistema de suministro eléctrico existente**. [Jung]
  * ## Descripción del problema
    * Generalmente el pronostico de la rapidez del viento y energía eólica  de las granjas de viento requiere el calculo del siguiente momento del estado definido, que es logrado basado en el estado de la atmósfera que engloba la presión atmosférica, temperatura, rugosidad y obstáculos cercanos. [Deng]
    * El establecimiento de modelos de rapidez de viento y energía eólica de alta precisión es siempre un desafío debido a la aleatoriedad, instantaneidad y características estacionales [Deng]
  * ## Wind SOTA
    * El rol básico del pronóstico de la rapidez del viento y la energía eólica es proveer información acerca de la rapidez del viento y energía que puede ser esperada en los siguientes minutos, horas, o días.
    * El pronostico de la rapidez del viento esta dividida en cuatro rangos temporales:
      * **Muy corto plazo **(pocos segundos a 30 minutos /1 hora)
        * **Configuración de turbinas eólicas,** información adicional sobre el mercado. [Freitas]
        * **Compensación del mercado eléctrico y las acciones reguladoras **[Lawan]
        * **Control de turbina y seguimiento de carga**. [Jung]
      * **Corto plazo** (una hora a dos días / 30 minutos a 6 horas)
        * Estimación económica de despacho de carga, **decisión sobre el incremento o disminución en energía**. [Freitas] 
        * **Despacho de potencia de salida de las turbinas eólicas para satisfacer con las necesidades del cliente** en poco tiempo [Lawan]
        * Para compartir precarga [Jung]
      * **Mediano plazo** (dos días a una semana / 6 horas a 1 día)
        * **Toma de decisiones sobre el apagado de turbinas eólicas** [Freitas]
        * Decisión de encendido/apagado de generadores eólicos, **seguridad operativa y para fines del mercado eléctrico**. [Lawan]
        * **Gestión del sistema de energía** y el comercio de energía [Jung]
      * **Largo plazo** (una semana a un año o más / un día a una semana o más)
        * **Apoya las decisiones en el mercado eléctrico y optimización de costos en la planificación de mantenimiento de las turbinas eólicas[Freitas]**
        * **Decisión de asignación de unidades**, cambiar la programación de mantenimiento [Lawan]
        * Programación de mantenimiento de las turbinas eólicas. [Jung]
    * En el presente, los modelos de predicción de rapidez de viento pueden se pueden dividir en tres categorías:
      * **Modelos de predicción físicos**
        * **Toman en cuenta el fenómeno meteorológico (o proceso meteorológico) y trata los cambios meteorológicos como eventos no aleatorios que satisfacen ciertas leyes físicas**. [Deng]
        * Un supuesto fundamental que en cualquier momento dado, la condición meteorológica (estado) es determinado por los datos atmosférica del pasado (historia). [Deng]
        * **Los cambios atmosféricos pueden ser simulados/calculados a través de la predicción meteorológica numérica (NWP), basada en la presión del aire, temperatura, irregularidades, contorno, y obstáculos alrededor de la granja eólica**. [Deng]
        * Estos modelos son capaces de predecir las variables deseadas directamente de los **datos en tiempo real**, haciendo los modelos preferidos para las granjas eólicas. [Deng]
        * **Requerir datos en tiempo real y de alta precisión, provoca una alta demanda por sistemas de adquisición de datos de alta precisión y redes de transmisión de datos de alta velocidad**. [Deng]
        * **El proceso de modelado tiende a ser complicado y sensible a los errores introducidos por las condiciones iniciales.** [Deng]
      * **Modelos de predicción estadísticos**
        * **Empiezan con ciertos fenómenos meteorológicos (o proceso), y los cambios meteorológicos en evolución son tratados como procesos aleatorios**. [Deng]
        * **En diferentes corridas pueden predecir diferentes resultados meteorológicos para las mismas condiciones de ambiente.[Deng]**
        * Dependen en el calculo de probabilidad de la ocurrencia de ciertas situaciones meteorológicas. [Deng] 
        * **Describen la relación entre los datos de entrada y salida para detectar patrones, a través del análisis de conjunto de datos masivo.** [Freitas]
        * Se consideran tres categorías [Freitas]:
          * Modelos de series de tiempo
            * **Modelo de Persistencia, AR, MA, ARIMA**
          * **Métodos de correlación espacial**
            * **Aprovecha las relaciones espaciales de los sitios vecinos. **[Frietas]
          * Métodos de Inteligencia Artificial:
            * **Redes Neuronales, Métodos de lógica difusa, K-nearest Neighbors, SVM**
      * **Modelos de predicción híbridos**
        * **Combinan en paralelo o secuencialmente, dos o más enfoques para poder describir el estado futuro de la rapidez del viento**.  [Frietas]
        * **En este enfoque la complejidad en desarrollo se vuelve mayor a medida que la combinación de métodos aumenta.** [Frietas]

    * **Es difícil decir cual modelo es el mejor debido a que cada modelo en uso tiene dependencias significativas del sitio (lugar físico). Entonces, un modelo de pronóstico puede funcionar bien en su sitio, pero esto no garantiza que el modelo funcione bien en otro sitio.** [Jung]
  * ## Objetivos
    * Mejorar la interpretabilidad de las series de tiempo de velocidad de viento con el uso de los mecanismos de atención
    * Mejorar la capacidad de aprendizaje de dependencias largas del modelo.
    * Mejorar el desempeño en la tarea de pronostico en cuanto al MAE y el RMSE.
  * ## Hipotesis
    * El uso de mecanismos de atención en un algoritmo basado en red recurrente mejorará el desempeño en la tarea de pronóstico de la rapidez del viento en comparación a una red sin mecanismos de atención.
  * # Redes recurrentes
    * RNN
    * LSTM
    * Multi-scale
  * # Mecanismos de Atención
    * Qué es?
      * La Atención, es motivada por como se presta atención visual a diferentes regiones de una imagen o palabras correlacionadas en una frase
      * En general, puede ser interpretado como un vector de pesos de importancia:
        * **Para predecir o inferir un elemento, éste se estima usando un vector de atención que nos indica que tan fuertemente esta correlacionado el elemento con otros elementos y toma la suma de estos valores ponderados por el vector de atención como una aproximación a la etiqueta.**
      * Los mecanismos de atención pueden indicar información relevante que es descartada por las redes neuronales. Además permite dinámicamente resaltar las características relevantes de los datos de entrada
      * **También pueden ser usados como una herramienta para interpretar el comportamiento de las redes neuronales.**
      * **Los mecanismos de atención se introdujeron en NLP debido a los problemas que presentaban los modelos seq2seq con el vector de contexto de largo fijo, que depende del último estado oculto del Encoder**
        * **Los problemas que se dan con el diseño del vector de contexto presentan desventajas por su incapacidad de recordar secuencias largas. Bahdanau et al. presenta un mecanismo de atención para resolver este problema**
      * Definición general
        * El núcleo de los mecanismos de atención es mapear una secuencia **K** a una distribución **a**
          * **K** (keys) puede ser una palabra o un embedding de caracteres de un documento, **o el estado interno de una RNN, o múltiple características  o representaciones del mismo objeto (e.g. un encoding one-hot y un emebedding de una palabra)**
          * **q** (query), es usado como una referencia para calcular la atentión.
            * **Puede ser un elemento único (estado oculto) o un rango de embeddings de textos, información de contexto, conocimiento de fondo.**
          * **V** (values) es dónde se aplica la atención, **junto con **K**, cada elemento pueden ofrecer dos, posiblemente diferente, interpretaciones de la misma entidad.**
      * ![[Roam/Turing/Attachments/imgs/app/Turing/NwZm_nCeJq.png]]
      * ![[Roam/Turing/Attachments/imgs/app/Turing/Un1kbDWsDt.png]]
    * Categorías de los Mecanismos
      * Self-Attention: Se relacionan diferentes posiciones de una sola secuencia para calcular una representación de la misma secuencia. Puede tomar cualquier función de *Alineamiento*, pero se remplaza la secuencia de slaida con la misma de entrada.
      * **Soft** Attention: the alignment weights are learned and 
placed “softly” over all patches in the source image; essentially the 
same type of attention as in [Bahdanau et al., 2015](https://arxiv.org/abs/1409.0473).
      * **Hard** Attention: only selects one patch of the image to attend to at a time.
      * The global attention is similar to the soft attention, while the local one is an interesting blend between [hard and soft](https://lilianweng.github.io/lil-log/2018/06/24/attention-attention.html#soft-vs-hard-attention)
      * **Self-Attention, es un tipo mecanismo de atención que relaciona diferentes posiciones de una sola secuencia para calcular una representación de la misma secuencia**. 
        * **El modelo realiza las predicciones de una parte de los datos de ejemplo usando otras partes de las observaciones acerca del mismo ejemplo.**
  * # Trabajo relacionado
    * Transformer
      * Modelo con arquitectura encoder-decoder, usado comunmente en modelos de Neural Machine Translation (NMT)
      * Hace posible el modelamiento seq2seq sin unidades recurrentes ( RNN/LSTM/GRU). Son construidos enteramente sobre mecanismos de self-attention sin usar una arquitectura recurrente de secuencia alineada. 
      * **Multi-head self-attention**
        * Es un modulo que es componente clave en el Transformer, en vez de calcular la atención una vez, el mecanismo multi-cabezal calcula el *scale dot-product attention* h veces en paralelo.
        * Esto permite al modelo poner conjuntamente atención a información de diferentes sub-espacios de representación en posiciones diferentes
      * ![[Roam/Turing/Attachments/imgs/app/Turing/rXtP6Bvo2V.png]]
    * Mejoras (familia transformer)
      * Mejoras al alcance de la atention
        * Transformer-XL
        * Alcance de atención adaptativo
      * Menor costo de tiempo y memoria
        * Sparse Transformers
      * Transformer tiene dos debilidades (En series de tiempo)Li:2019
        * *locality-agnostics*: El *point-wise dot product self-attention* en el Transformer Vanilla es insensible al contexto loca, lo que hace que el modelo sea propenso a anomalias en series de tiempo.
        * *Cuello de botella en memoria*: El espacio de complejidad del *Transformer* crece cuadraticamente con el largo de la secuencia L, haciendo directamente modelar series de tiempo largas inviable
        * Aplican exitosamente el Transformer en el pronostico de series de tiempo, con experimentos en datasts sintéticos y reales para validar la arquitectura en manejar de mejor forma las dependencias de largo plazo que los modelos basados en RNN
        * *Convolutional self-attention*: Utilizan mecanismos de convolución causal para producir las queries y Keys en la capa de self-attention. Logrando una concordancia query-key consiente del contexto local.
          * ![[Roam/Turing/Attachments/imgs/app/Turing/rg2heA_v35.png]]
        * *LogSparse* Transformer, con una complejidad espacial O(L(log L)^2)  para romper el cuello de botella, no solo haciendo el modelamiento de las series de tiempo largas con granularidad más fina factible sino también produciendo resultados comparables o mejores con muchos menos uso de memoria
        * ![[Roam/Turing/Attachments/imgs/app/Turing/Mc-d5EHERz.png]]
        * ![[Roam/Turing/Attachments/imgs/app/Turing/JzfWeSRJby.png]]
    * Wind Power Forecasting Methods Based on Deep Learning: A Survey
    * Deep learning para (Wind speed forecating)
      * En la literatura se han investigado y utilizado métodos de análisis de aprendizaje profundo, aprendizaje reforzado y *transfer learning*
      * **RNN LSTM**
        * Las RNN y LSTM predicen la secuencia de tiempo a lo largo del tiempo, lo que indica que antes de que la información ingrese a la unidad de procesamiento actual, la información a largo plazo de la secuencia de entrada debe ser previamente recorrida por todas las unidades de capa ocultas en orden.
        * El gradiente asociado puede sufrir de problemas de gradiente desvaneciente o gradiente explosivo, por lo que la adquisición de información a largo plazo para secuencias es aún un desafío.
        * En general las redes LSTM o Elman se ocupan en combinación con alguna técnica de descomposición o transformación en la fase de preprocesamiento de los datos, dentro las más populares son las en base a wavelets.
        * Además las arquitecturas multi-escala en combinación con las LSTM han demostrado mejorar el aprendizaje de dependencias largas manteniendo eficiencia computacional
      * **ELM o SELM**
      * CNN o DBN
      * Enfoque Red neuronal Híbrido 
      * Q-learning
    * Low computation attention
      * Single Headed Attention RNN (SHA-RNN)
        * ![[Roam/Turing/Attachments/imgs/app/Turing/VTgsNvWW3v.png]]
        * El modelo consiste en una capa de embedding entenable, una o más capas de un stack de SHA-RNN y una capa softmax
        * La motivación se basa en que no hay una clara relación entre el rendimiento del modelo y la cantidad de cabezales que éste posea.
  * # Propuesta
    * LSTM-Attention 
    * Transformer block Sparse attention
    * Low resource LSTM attention
    * Low resource Multi-scale LSTM attention
  * # Experimentos
    * Dataset
      * Datos del Ministerio de Energía en el Norte de Chile, obtenidos de una torre de prospección eólica bajo el nombre de e01
      * e01 25719 ejemplos
      * La separación del conjunto de datos es de 80% 10% 10%
      * Se utilizan las métricas del MAE y RMSE sobre el conjunto de pruebas
    * Persistencia *
    * SARIMA *
    * Stacked LSTM *
    * Transformer *
    * Transformer encoder block - Stacked LSTM *
    * Single Attention head LSTM +
    * Single Attention head Multi-scale LSTM +