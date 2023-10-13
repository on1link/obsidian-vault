  * **Constant Error Carousel**
    * Vanilla LSTM's that don't have a forget gate and instead are added an unchanged cell state (e.g. A recurrent connection with a constant weight of 1)
  * **Vanishing Gradient Problem** ^17qg8_qCL
    * TBD
  * **Time Step**
    * Un dato de la secuencia que se entrena en el tiempo $$t$$
  * **Rolling Forescast**
    * Also called *Walk-foward* model validation
    * Cada paso de tiempo del conjunto de test será caminado un paso a la vez. 
  * **Diferencia entre entrenamientos de LSTM**
    * ```1:for i in range(10): #training
    model.fit(trainX, trainY, epochs=1, batch_size=batch_size, verbose=0, 
              shuffle=False)
    model.reset_states()

2:
model.fit(trainX, trainY, epochs=10, batch_size=batch_size, verbose=0, 
          shuffle=False)```
    * En ambos casos, el modelo es entrenado por 10 epochs. Durante cada epoch, todos los ejemplos en tu conjunto de entrenamiento fluyen por la red. El tamaño del batch determina el número de ejemplo después de los cuales se actualizan los pesos o parámetros del modelo.
    * La diferencia entre el primero y segundo caso es que el primero permite algo de procesamiento afuera del método `fit()` entre los epochs, tales como `model.reset_states`. Sin embargo, procesamiento similiar puede realizarse en el segundo caso mediante la clase de callbacks personalizada, que incluye por ejemplo, funciones `on_epoch_begin`, `on_epoch_end`, `on_batch_begin` y `on_batch_end`.
    * Sin el método `model.reset_states()` los resultados debieran ser los mismos respetando corriendo los modelos con al misma semilla por separado.
    * Cuando has alcanzado el tamaño total de las secuencias, entonces tu llamas `model.reset_states()`, que significa que no continuaras con las secuencias previas más, ahora se alimentaran nuevas secuencias.
  * **Shallow Linguistics processing**
    * Los enfoques de aprendizaje automático (también conocidos como procesamiento lingüístico superficial) han alterado fundamentalmente el campo del procesamiento del lenguaje natural.
  * **Metrica** $R^2$
    * El coeficiente $R^2$ está definido como: $$ R² = (1 - \frac{u}{v})$$donde $u$ es la suma residual al cuadrado: $$ u = \sum (y_{true} - y_{pred})^2 $$ y $v$ es la suma total de los cuadrados: $$ v = \sum (y_{true} - \overline{y}_{true})^2$$
    *  El mejor valor posible para el *score* es $1.0$ y puede ser negativo (debido a que el modelos puede ser arbitrariamente peor).
    * Un modelo constante que siempre predice el valor esperado de $y$, sin 
importar las características de entrada, obtendrá un $R^2 = 0.0$
  * *Combinación Convexa* (Matemática)
  * **Degree day**
    * **Degree** **days** are a useful metric for estimating energy consumption required for household heating and cooling, and in this context are formally referred to as heating **degree** **days**.  Since the escape or ingress of heat due to conduction is proportional to the difference between the indoor and outdoor temperature, the amount of energy needed to maintain the base temperature indoors for some period of time is roughly proportional to the number of **degree** **days**.
  * 
