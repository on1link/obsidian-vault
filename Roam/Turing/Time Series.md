  * Una serie de tiempo es una serie de datos puntuales ordenados en el tiempo.
  * En una serie de tiempo, generalmente el tiempo es la variable independiente y el objetivo es usualmente realizar un pronóstico del futuro. 
  * Time series can vary depending on the **number of input and output sequences, the number of steps to forecast, and whether the input sequence length is static or variable.**
  * ## Types of time series forecasting problems
    * In total there are at least 18 different types of time series problems based on the following variations or building block:
    * ### Number of Input and Output Sequences
      * You can either have a single time series or multiple time series as an input
      * **Univariate** time series problems.
        * In a univariate time series problem, you only have one time series which is used as the input sequence and as the output sequence as well.
        * ` input_cols = ["energy_consumption"]
  output_cols = input_cols
`
        * Example: Forecasting the future energy consumption of a building based on its past consumption.

      * **Multivariate** time series problems.
        * For multivariate problem formulation, we also differentiate between **equal and different input and output sequences**
        * **Multivariate with Equal Inputs and Outputs**
          * In a multivariate time series problem, you can have multiple time series which are used as input sequences and as output sequences as well.
          * `input_cols = ["temp_1", ..., "temp_n"]
output_cols = input_cols`
          * You would usually use this problem formulation when there is a correlation between multiple time series.
          * Example: Forecasting the future temps at different altitudes in a region based on past registers. 
        * **Multivariate with different inputs and outputs**
          * You can also have different input and output sequences.
          * `inputs_cols = ["precipitation", "temperature"]
output_cols = ["snowfal"]`
          * You would usually use this problem formulation if you need additional information from another time series to forecast the target sequence. E.g. you provide some time awareness by feeding a module or sine wave signal to the model).
          * Example:  Forecasting the amount of snowfall based on previous precipitation and temperature.
    * ### Length of Output Sequences
      * Look at the length of the output sequences (sides). That means you can either forecast a single time step or multiple time steps into the future.
      * We have **single-step and multistep** time series problems. And for the multistep problem formulation, we have differentiate between **single-shot and recursive predictions**
      * **Single Step Output Sequence**
        * The single-step time series problem is the easiest because you only have to forecast one timestep into the future
        * Example: Forecasting the number of goods to bake for the next day. 
      * **Single-shot Multistep Output Sequence**
        * Multistep time series problem is a little bit harder because you have to forecast more than one timestep into the future. The further in the future we try to forecast at once, the less reliable our predictions become
        * Example: Forecasting the number of school lunches for the next week to buy the right amount of groceries.
      * **Recursive Multistep Output Sequence**
        * Instead of forecasting multiple timesteps into the future at once, you can forecast single timesteps. Meanwhile forecasting one timestep is more reliable than forecasting multiple timesteps at once, keep in mind that in this method you will carry over the error from the previous prediction (cumulative error)
    * ### Type of Input Sequence
      * You can either use an input sequence with a fixed lenght or you can have an input sequence with a variable length.
      * We differentiate between the **sliding window and expanding window** time series problems.
      * Another factor to consider is the **step size**. While you could shift or expand your sequence window one timestep at a time, you could shift it by a few timestepts at a time as well. The smaller you stepsize, the higher the number of available training samples.
      * **Sliding Window**
        * Sliding window means that **your input sequence** always has a specified **fixed length**, e.g. one hour, one day, one week, six months, one year, five years, etc.
        * Example: Forecasting the demand for school lunches for school lunches for the next year based on the previous year.
      * **Expanding Window**
        * The length of the input sequences increases for the expanding window time series problem.
        * Example: Forecasting the number of new users on a platform for the next month based on all historical data.
  * # Exponential Smoothing
  * # Tendencia (Trend)
  * # Estacionariedad (Stationary) 
    * Es una característica importante de las series de tiempo.
    * Una serie de tiempo se dice ser estacionaria si sus propiedades estadísticas no cambian en el tiempo. Tiene **media y varianza constantes**, y la co-varianza es independiente del tiempo.
    * A menudo, precios stock no son procesos estacionarios, ya que se pueden ver tendencias crecientes, o su capacidad de cambiar puede aumentar en el tiempo (significa que la varianza esta cambiando)
    * Idealmente queremos series de tiempo estacionarias para modelar, pero se pueden realizar diferentes transformaciones para dejarla estacionaría.
    * ## Probar si un proceso es estacionario.
      * Test *Dickey-Fuller*, test estadístico para determinar si una serie de tiempo es estacionaria o no.
        * Prueba la hipótesis nula que una raíz unitaria esta presente. **(VERIFICAR)**
        * *Si la hay, entonces $$ p > 0 $$, y el proceso es no estacionario.*
        * *De otra manera, $$ p=0 $$, la hipótesis nula es rechazada, y el proceso es considerado ser estacionario. *
        * Ejemplo:
          * ![[Roam/Turing/Attachments/imgs/app/Turing/NTnIT733KZ.png]]
  * # Estacionalidad (Seasonality)
    * Se refiere a fluctuaciones periódicas.
    * Ejemplo: 
      * El consumo eléctrico es alto durante el día y bajo durante la noche.
      * Las ventas en línea aumentan durante la Navidad antes de disminuir lentamente de nuevo.
    * ![[Roam/Turing/Attachments/imgs/app/Turing/cB_mFizBw9.png]]
      * En el gráfico, se observa claramente estacionalidad.
      * Cada día, se aprecia peaks hacia el atardecer, y en los puntos más bajos son al iniciar y al terminar cada día.
    * La estacionalidad puede ser derivada también desde un gráfico de autocorrelación si este tiene una forma sinusoidal.
    * Mirando el periodo, se puede saber el largo de la estación.
  * # Autocorrelación (Autocorrelation)
    * Informalmente, la autocorrelación es la similitud entre las observaciones en función del intervalo de tiempo (lag) entre ellas.
    * ![[Roam/Turing/Attachments/imgs/app/Turing/eaQ82gNGv9.png]]
    * Ejemplo: 
      * En el gráfico de autocorrelación se observa que el primer valor y el 24vo valor tienen una alta autocorrelación. 
      * De manera similar ocurre con las 12va y 36va observaciones son altamente correlacionadas.
      * Esto significa que podremos buscar valores similares cada 24 unidades de tiempo.
      * Notar la forma sinusoidal del gráfico. Ésto es una pista de estacionalidad
  * # Autocorrelación Parcial (Partial Autocorrelation)
  * # Modelamiento de Series de Tiempo
    * Hay muchas formas de modelar una serie de tiempo para poder realizar prónostico
    * ## Modelos ARIMA
      * ## Media Móviles (Moving Average MA):
        * El enfoque más ingenuo (naive) de modelamiento de series de tiempo
        * El modelo simplemente afirma que la siguiente observación es la **media de todas las observaciones pasadas**
        * De otra forma, MA puede ser usado para identificar tendencias interesantes en los datos.
        * Se puede definir una *ventana* para aplicar el modelo de media móvil para *suavizar* la serie de tiempo, y destacar diferentes tendencias.
        * ![[Roam/Turing/Attachments/imgs/app/Turing/omSrFXiFDA.png]]
          * Modelo MA con ventana de tamaño 24h. 
          * La línea verde *suaviza* la serie de tiempo, y se pueden ver 2 picos en un periodo de 24h.
          * Entre más grande la ventana, más *suave* la tendencia será.
          * ![[Roam/Turing/Attachments/imgs/app/Turing/ULye8iUp1d.png]]
      * ## AutoRegressive (AR):
        * Esta parte explora cualquier relación dependiente entre una observacion y algún número de variables retrasadas (lagged)
        * En primer lugar están los modelos **AutoRegresivos AR(p)**.
          * Es básicamente una regresión de la serie de tiempo en si misma
          * Se asume que los valo res actuales dependen de sus valores previos con algún retraso (lag).
          * Toma el parámetro $$p$$ que representa el retraso máximo. Para encontrarlo se busca en el gráfico de autocorrelación parcial (PAC) y identificar el retraso en el cual la mayoría de los retrasos no son significativos.
          * Ejemplo $$p=4$$ en gráfico de autocorrelación parcial:
            * ![[Roam/Turing/Attachments/imgs/app/Turing/8G1oRQwqoD.png]]
      * ## ARIMA
        * Box-Jenkins ARIMA (Auto-Regressive Integrated Moving Averager)
        * Enfoque popular para modelar sistemas dinámicos
        * Modela las variables observadas $$x_t$$ y asume que $$x_t$$ puede ser descompuesto en los componentes de tendencia (trend), estacionalidad (seasonal), e irregulares. [[Wu, N.2020 Deep Transformer Models for Time Series Forecasting The Influenza Prevalence Case]]
        * En vez de modelar los componentes por separado, la idea es diferenciar la serie de tiempo $$x_t$$ de manera de eliminar la tendencia y la estacionalidad. El resultado es tratado como una series de tiempo estacionaria.
        * Ver [[Roam/Turing/Time Series#^cLSUGQhUF|SARIMA]]
      * ## SARIMA
        * Modelo **SARIMA(p, d, q)(P, D, Q, s)**
        * Es una combinación de modelos más simples para crear un modelo más complejo que puede modelar series de tiempo que exhiben propiedades no estacionarias y estacionalidad.
        * Se añade el modelo de [[Roam/Turing/Time Series#^hVdyTRDDq|Media Móviles (Moving Average MA):]] **MA(q)**.
          * Toma el parámetro $$q$$ que representa el mayor retraso después del cual los otros retrasos no son significativos en el gráfico de autocorrelación.
          * Ejemplo $$q=4$$ en gráfico de autocorrelación:
            * ![[Roam/Turing/Attachments/imgs/app/Turing/fs77ihvJjl.png]]
        * Se añade el **orden de integración I(d)**.
          * Toma el parámetro $$d$$ que representa el número de diferencias requeridas para que la serie sea estacionaria.
        * Finalmente, se añade el componente de [[Roam/Turing/Time Series#^COlXptt5O|Estacionalidad (Seasonality)]] **S(P, D, Q, s)**
          * El parámetro $$s$$ es simplemente el largo de la temporada
          * $$P$$ y $$Q$$ es lo mismo que $$p$$ y $$q$$, pero de la componente estacional.
          * Finalmente $$D$$ representa el número de diferencias requeridas para eliminar la estacionalidad de la serie.
        * Combinando todo obtenemos nuestro modelo SARIMA(p, d, q)(P, D, Q, s)
        * El principal punto a recordar es que antes de modelar con SARIMA, se deben aplicar transformaciones a la serie de tiempo para eliminar la estacionalidad y cualquier comportamiento no estacionario.
