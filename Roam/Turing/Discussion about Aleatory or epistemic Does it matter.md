  * Requerimientos
    * Exposición general del tema
    * Aspectos relacionados con la ciencia, la técnica y la tecnología.
    * Marco teorico conceptual precisando conceptos
    * Conclusiones personales.
  * Extra:
    * Explicar conceptos y supuestos de la discusión
    * Explicitar el origen de la información o de otros documentos utilizados
  * # Resumen
  * # Formulación de la problemática
    * Dado que en general los problema de ingenieria son resueltos desde el mundo de universos de modelos. Estos modelos contienen un conjunto de modelos fisicos y probabilisticos que son empleados ocmo idealizaciones matematicas de la realidad para dar con una solución para el problema a mano. 
    * Este universo de modelo puede contener  inheremntemente incertidumbres. Por lo que una importante parte de construir estos modelos es modelar estas incertidumbres. Los autores argumentan que este proceso lleva un elemento significativo de subjetividad. "Los ingenieros se destacan cuando, dado un tiempo limite, sus modelos concebidos resultan estara cerca de la realidad."
    * Desde esto toda incertidummbre, ya sea su naturaleza o caracterización debe estar confinada en este universo de modelos (supuesto fuerte).
    * Dado que los problemas de ingenieria de interes involucran los dos tipos de incertidumbres . Se ha sugerido que se necesita una calra distinción entre estas incertidumbres.
      * El problema surge en la fase de modelado, dado que es dificil determinar cuando una incertidumbre en particular debe corresponder a la catergoria aleatoria o la categoria epistemica.
      * Los autores son partidarios de que el autor del modelo debe hacer esta distinción.
        * Esta decisión es condicionada al estado general del conocimiento cientifico y de los datos disponibles (Fuerte relacion con Ciencia tecnologia y tecnica)
        * Pero a su vez a la necesidad practica de limitar la sofisticación de un modelo al nivel de una importancia significativa de la ingenieria para las decisiones que producen el modelo
    * En primer lugar los autores mencionand que la naturaleza de las incertidumbres y como se gestioanen dependen del contexto y la aplicación. En este sentido hace incapie que depende del creador del modelo caracterizar apropiadamente estas incertidumbres.
  * ## Conceptos
    * Incertidumbre epistemica
      * Se caracteriza por aquelaa en el cual el creador del modelo ve la posibilidad de reducirlas recolectando más datos o refinando los modelos. Ademas se presume que es debido a la falta de conocimeinto (o datos).
      * Tambien da cuenta de la incertidumbre del modelo, es decir, de sus parametros, la cual captura nuestra ignoracia sobre el modelo generado por nuestros datos recolectados y como se menciono anteiormente puede ser explicada a medida que se obtienen màs datos. También es conocida como la incertidumbre del modelo[2]
      * Desde el punto de vista de la ingenieria es ùtil ya que esta inceridumbre puede ser representada en el modelo introduciendo variables auxiliares no fisicas.
        * Un punto importante de estas variables auxiliares definen las depencias estadisticas (correlaciones). que surgen entre diferentes componentes de un problema que tienen incertidumbres comunes, de manera clara y transparente.
    * Incertidumbre aleatoria
      * Se caracterizan por aquellas incertidumbres en las cuales el creador del modelo no puede ver la posibilidad de reducirlas. Ademas se presume que es parte intrinsica del la aleatoriedad del fenomeno.
      * Estas capturan el ruido inherente en las observaciones. Esto puede ser a través de ruido capturado en los intrumentos, resultando en una incertidumbre que no puede ser reducida incluso si más datos son recolectados. Tambièn esta incertidumbre puede ser categorizada como incertidumbre *homoscedástica*, la cual es incertidumbre que se mantiene constante para distintas entradas del modelo, ó *heterodástica* la cual es incertidumbre que depende de las entradas del modelo, con algunas entrada potenciamlente teniendo más ruido que otras.[2]
    * Es importante recalcar que ambos tipos de incertidumbre no son mutuamente exluyente [2]
    * Fuentes de incertidumbre
    * Categorización de las incertidumbres
  * Problema entre las incertidumbres en el ambito de la ciencias, tecnica y tecnologia
  * Agregar problema en la ingenieria
  * # Marco teórico (Estado del Arte)
  * Mencionar top 5 articulos que citan a este aritculo
    * En [2] realizan una aplicación de esta categorización de las incertidumbres a través de el modelado Bayesiano a un problema de Aprendzaje profundo Bayesiano aplicado a Computer Vision. Las contribuciones que lograron usando esta aproximaciòn fueron capturar un entedimiento preciso de las incertidumbres aletaroias y epistemicas, mejorando entre un 1% a 3% el rendimiento del modelo sobre modelos bases no bayesianos reduciendo el efecto de los datos con ruidos con la atenuaciòn obtenida de explicitamente representar la incertidumbre aleatoria. También hace incampie en la importancia de modelar ambas incertidumbres:
      * Incertidumbre Aleatoria:
        * Siaciones con grnades candidades de datos, donde la incertidumbre epistemica puede ser explicada
        * Aplicaciones en tiempo real, debido a que podemos generar modelos aleatorios sin muestras a través del Método de Monte Carlo
      * Incertidumbre espistamica:
        * Aplicaciones de seguridad critica, ya que la incertidumbre epistemica es necesaria para entender los ejemplos que son distintos a los datos de entrenamiento.
        * Para pequeños conjuntos de datos, donde los datos de entrenamiento es escasa.
  * Mencionar 5 articulos relacionados con incertidumbre epistemica y/o aleatoria y la ciencia, técnica y tecnología
    * En el aspecto de Ciencia, Técnica y Técnologia tenemos a [3] que nos detalle como el rendimiento de un sistema multidisciplinario es affectado por varias fuentes de incertidumbre. Usando el metodos de analisis de sensibilidad estadistica permiten el estudio del impacto de distintas fuentes de incertiduembre en el rencimiento del sistema. Aplicar este tipo de analisis es sistemas multidisciplinario es un desafio mayoy dada la complejidad en el analisis del sistema como tambiñen a las interaciones acopladas entre los subsistemas. Con lo cual pueden concluir la importancia 
 de este tipo de analisis puede jugar en la optimización del diseño multidisciplinario, ayudando a los diseñadores a tomar decisiones sobre cuando simulaciones o datos experimentales o mejoras en el modelo son necesarias para reducir la incertidumbre epistemica del modelo.
  * # Hipótesis o Hipótesis formulada en el articulo
    * ¿Cuales son los objetivos o preguntas de investigación?
      * ¿Incertidumbre aleatoria o espistemica? ¿Importa?
      * ¿La incertidumbre aleatoria puede transformarse en epistemica a medida que tenemos mejor calidad de los datos?
    * Hipotesis
      * La distinción entre incertidumbre aleatoria y epistemica es determinada por nuestros alternativas de modelado. La distinción es util para identificar fuentes de incertidumbre que pueden ser reducidas en el corto plazo, esto es, sin esperar que ocurran grandes avances en el conocimiento cientifico, y en desarrollar riesgos de sonidos y modelos de  fiabilidad.
  * # Objetivos específicos
    * Demostrar la importancia de una apropiada caracterizacion de las incertidumbres ya sea aleatoria o epistemica de un modelo dado puede ayudarnos a reducirlas en el caso que sea epistemica. Además de prevenir que estas incertidumbres puedan introducir dependencias entre enventoss aleatoreos
    * Reabrir la discución en el contexto de fiabilidad estructural y análisis de riesgos.
    * Demostrar que la distinción de estas fuentes de incertidumbre es util para resolverlas a corto plazo, en pesra de avances en el conocimiento cientificio (esto es imporante desde le punto de vista de la ciencia y la tecnologia y su avance en relación a la generación de nuevo conocimiento)
    * Demostrar la utilidad para la transparencia en al toma de decisiones, ya que puede mostrarnos cuales incertidumbres han quedado sin reducir como consecuencia de nuestras dediciones.
  * # Discusión
    * Desde las categorizaciones de la incertidumbres que dan los autores e incluso ellos mismo lo remarcan al final de la lectura de la categorización de las incertidumbres es, ¿realmente existe alguna incertidumbre aleatoria? Dado que se remarca el hecho que las incertidumbres son una falta de conocmieto o datos. Sin embargo argumentan de buena manera que esto se da en u mundo utoptico, que esta muy lejos de la realidad de la ingeniera a día de hoy.
    * Otro punto a destacar sobre el punto anterior es la consecuencia a la cual esta categorización resulta ùtil para poder distribuir los recursos que se necesiten y en desarrollas modelos de ingenieria.
    * Dada la subjetividad de la creación de modelos se comparte la visión de los autores al decir que la ingenieria constituye un "arte" y que es uno de los elementos más descatado de la practica. Esto nos lleva nuevmanet a la discución del curso y de como se genera el conocimiento, dando a conocer que la ciencia también es un arte o que puede nacer desde el arte.
    * Los ejemplos dados y datos sugieren un problema desde el punto de vista de como se deben abordar los problemas hoy en día, en primer lugar debido a que estos problemas se representan y se deben asumir que son complejos y que sus interacciones son no-lineales. En segundo lugar los ejemplos plantean que en sistemas y subsistemas redundantes o en paralelo (no en serie) el efecto que tienen de la incorrecta categorización puede ser en ordenes de magnitud mayor. Dado que hoy en día la mayoría de los problemas son de orden complejos, se recalca más aún la discución que plantean los atuores.
    * En base a lo discutido se puede recomendar, para la formulaciones de los problemas a estudiar en futuras investigaciones es necesario considerar la categorizacion de estas incertidumbres debido a las ventajas presentadas anteriormente, dado que se puede aplicar en varias areas de la ingeniera, como por ejemplo, en aprendizaje profundo.
    * Es necesario ver también cuales son los alcances y limitaciones  se pueden obtener de este tipo de categorizaciòn y la complejidad del sistema que se requiere modelar.
  * # Conclusiones

  * # Referencias