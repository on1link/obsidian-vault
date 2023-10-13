  * # Abstract
    * To efficiently manage unstable wind power generation, precise short-term wind speed forecasting is critical. To overcome the challenges in wind speed forecasting, this paper proposes a new convolutional neural network algorithm for short-term forecasting. In this paper, the orecasting performance of the proposed algorithm was compared to that of four other artificial intelligence algorithms commonly used in wind speed forecasting. Numerical testing results based on data from a designated wind site in Taiwan were used to demonstrate the efficiency of above-mentioned proposed learning method. Mean absolute error (MAE) and root-mean-square error (RMSE) were adopted as accuracy evaluation indexes in this paper. Experimental results indicate that the MAE and RMSE values of the proposed algorithm are 0.800227 and 0.999978, respectively, demonstrating very high forecasting accuracy
  * ## Notas
    * ### Primera pasada:
      * **Categoría**: ¿Qué tipo de articulo es éste? ¿Un articulo de medición? ¿Un análisis de un sistema existente? ¿Una descripción de un prototipo de investigación?
        * Articulo de medición.
      * **Contexto:** ¿Con qué otros artículos está relacionado? ¿Qué bases teóricas se usaron para analizar el problema?
        * N/A, Bases teorícas de las CNN y técnicas de Machine learning.
      * **Exactitud** (*correctness*): ¿Los supuestos parecen ser validos?
        * Parecen validos, datos de training y testing por separado, falta especificar bien el baseline y modelos a comparar. Se mencionan muchos articulos en la introducción referente a métodos de Machine Learning y distintos tipos de problemas de  Wind Speed Forecasting  (short-term, long-term)
      * **Contribuciones**: ¿Cuáles son las principales contribuciones del artículo?
        * Un nuevo tipo de modelo para el pronostico de viento, mejorando en MAE y RMSE los datos de viento de la locación especificada en el paper.
      * **Claridad**: ¿Está bien escrito el documento?
        * No, introducción y repaso de métodos poco agrupados no hay una tabla comparativa o algo al respecto, no se entiende la intención de mencionar tantos métodos que no se mencionan en experimentos (decission trees, random forest, svm, mlp, cnn).
  * ## Referencias
    * [[Jung2014 Current status and future advances for wind speed and power forecasting]]