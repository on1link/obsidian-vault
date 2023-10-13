  * # Introduction
  * # Theoretical Framework
  * # Related Work
  * # Datasets
    * Low Carbon London Project (LCLP): Consumo de casa o industrias bajo regímenes de incentivo a la demanda (cambios de precios a lo largo del día)
      * Using smart meters and substation sensors to facilitate smart grids
      * Sought to determine how smart meter and substation sensor data could be used to better understand the way in which customers contribute to network load.
      * The project deployed 5.533 smart meters. During the trials half-hourly meter reading data for the full 2013 calendar year.
      * An important feature of this full dataset was the demographic profiling that was obtained for all households. 
      * The dataset we are using contains almost forty thousand examples (39727) and 5198 columns, where each columns represent a smart meters (Verify source)
    * Global Energy Forecasting Competition (GEFCom) 2012, 2014, 2017 : Competencia de pronóstico de energía con ese nombre. Son de demanda de una industria de EEUU*.
      * The topic of the probabilistic electric load forecasting track is to forecast the probabilistic distribution (in quantiles) of the hourly loads for one utility on a rolling basis.
      * Data: Hourly historical load and weather data of the utility are provided. The incremental data is being released every week. The forecast horizon is **one month**.
      * Submit probabilistic forecasts in the form of quantiles, 99 quantiles for each step throughout the forecast horizon.
      * Evaluation Metric:
        * Pin ball function will be used to evaluate the accuracy of the probabilistic forecasts.
    * UCI: Individual Household Load Demand, una casa (o éste caso es una industria*)
    * Electricity: Montón de casas en Portugal, en todos lados llaman a este conjunto 
    * Todos son públicos, usados en la literatura y fácilmente descargables en su versión raw.
    * Nacionales
      * Wind*: Son velocidad de viento, descargado del antiguo explorador de datos
      * Los totoral y canela que son potencia eólica generada por la central correspondiente (Canela son dos)
      * Substation: Son demanda eléctrica a nivel de subestación eléctrica en Chile (Unas poquitas mejor comportadas)
  * # Proposal