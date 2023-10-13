  * # Golden Thread
    * ## Research aim
      * Review recent work related to the modeling and prediction of building energy consumption.
    * ## Research objectives
      * Describe methods, including engineering, statistical and artificial intelligence methods.
      * Especially focus on the the prediction applications
      * Review engineering and statistical methods, and some hybrid approaches
      * Describe applications, models, related problems such as data-preprocessing
    * ## Research Questions
  * # Introduction
    * ## Problem:
      * Buildings account for 40% of total energy use and 36% of total CO2 emission.
      * The energy system in buildings is quite complex, as the energy types and building types vary greatly.
      * In literature the main energy forms considered are heating/cooling load, hot water ans electricity consumption. 
    * ## Building types
      * Office, residential, engineering buildings
      * The energy behaviour of a building is influence by many factors.
    * The whole building or sub-level component can be predicted by thoroughly analyzing each influencing factor or approximating the usage by  considering several major factors.
      * Weather conditions, building characteristics, and thermal property of the physical materials.
  * Recent work related to modeling and prediction of building energy consumption.
    * These method include **engineering**, **statistical** and **artificial intelligence**
      * Artificial Intelligence: [[Artificial Neural Networks]] (ANN), [[Support Vector Machines]] (SVM)
    * The paper focuses in prediction applications. And provide some hybrid approaches to optimize predictive performance.
    * Globally describe the applications, models, related problems such as data pre-processing, and future prospects.
  * # The prediction methods
    * ## Engineering methods
      * The engineering methods use physical principles to calculate thermal dynamics and energy behaviours.
      * These methods can be roughly classified in two categories
        * Detailed comprehensive method
          * Use very elaborate physical functions or thermal dynamics to calculate the energy consumption for all components, with the building's and environmental information (external climate conditions, building construction, operation, utility rate schedule, HVAC equipment) as inputs.
          * Hundred of software tools have been developed for evaluating energy efficiency, renewable energy, and sustainability in buildings.
        * Simplified method
          * Almost all simpler models use weather data to **calculate energy consumptions** based on average temperatures or temperatures bins; atmosferic pressure, humidity, solar radiation, wind speed.
          * Building characteristic is another important factor to determine energy performance.
          * The method of predicting a **daily energy consumption profile** for the design of a renewable energy system for residential buildings was developed by Yao and Steemers (ref).
          * Other methods use divide-and-sume concept to **estimate each component consumptions** with simpler estimation and sum up to get the building performance and explain **the system level building energy consumption**
      * Calibration is an important issue in building energy simulation. Since  calibration is a tedious and **time-consuming work** , we can see that doing accurate simulation by a detailed engineering method is of **high complexity**.
    * ## Statistical methods
      * The regression models correlate the energy consumption with the variables. 
      * Statistical regression models simply correlate the energy consumption or **energy index** with the influencing variables. These empirical models are developed from historical performance data.
      * The research on regression models has been focus on three problems:
        * Predict the **energy usage** over simplified variables such as one or several **weather parameters**.
        * Predict some useful **energy index**.
        * Estimate important **parameters of energy usage**
          * Heat loss coefficient, total heat capacity and gain factor, which are useful in analyzing thermal behavior of building or sub-level systems.
      * Regression models to:
        * Correlate energy consumption with the climatic variables to obtain an energy signature
        * Handle both heating and cooling calculations simultaneously.
        * Calculate the cooling load of a building by adding up the cooling load of each component of the building envelope.
          * Each sub-level cooling load is a regression function of temperature difference between inside and outside the building.
        * Model heating and cooling load in commercial buildings with outdoor dry-bulb temperature as the only weather variable
        * Predict energy savings from retrofit projects of office buildings in a hot summer and cold winter region.
        * Predict monthly power energy consumption for large scale public buildings.
      * For **energy index**, the PCA was used to develop a climatic index Z for global solar radiation, dry-and wet-bulb temperature.
      * An ARIMA model was used to predict load profiles for the next day.
        * It implement on-line prediction. 
        * **Use past load data**
      * An ARIMAX model was use to
        * predict and control the peak electricity demand for commercial buildings
        * **predicting the power demand of the buildings** by Newsham and Birt
          * with emphasis on the influence of occupancy, which can apparently increase the accuracy of the model.
    * ## Neural Networks
      * [[Artificial Neural Networks]] are the most widely used artificial intelligence models. This type of model can be used to solve **non-linear** problems. 
      * ANNs are used to 
        * Analize and improve sub-level components.
        * **Predict energy consumption** in office buildings.
      * Neural Networks can achieve higher prediction performance than engineering models when estimating appliance, lighting and space cooling **energy consumption** in the Canadian residential sector. 
      * It is better than the conventional non-linear regression models.
      * Used to analyze various types of building energy consumption, sub-level components operation and optimization, estimation of usage parameters.
      * There are groups according to the applications dealt with.
      * Use of ANN to:
        * Energy application in buildings: 
          * Solar water heating systems
          * Solar radiation
          * wind speed
          * air flow distribution inside a room
          * prediction of energy consumption, indoor air temperature
          * HVAC system analysis
        * Predict:
          * The required heating load of buildings
          * Building heating loads
          * The annual heating demand of a number of small single family buildings
          * Make long-term (annual heating demand) energy demand prediction based on short-term (2-5 weeks) measured data 
          * Cooling demand in a building
          * Building heating and cooling energy needs in the future, knowing only the weather and time stamp.
          * The cooling load of three office buildings
          * Energy consumption of a passive solar building
          * Building's heating and cooling load in different climate zones represented by heating degree day and cooling degree day
        * The application of building energy usage prediction:
        * Predict
          * Hourly electricity consumption as well as chilled and hot water for an engineering center building.
          * Relate the electric energy consumption to the number of occupancy and weather data
          * Short-term electricity load with a special neural network which feeds back part of its outputs.
          * Long-term annual electricity consumption in energy intensive manufacturing industries
          * Energy consumption for office buildings with day-lighting controls in subtropical climates. The output include daily electricity usage for cooling, heating, electric lighting and total building.
        * Analyze and optimize sub-level components behavior, mostly for HVAC systems.
        * Predict
          * Air-conditioning load in a building
          * Detect and diagnose faults in a building's air-handling unit.
          * Estimate appliance, lighting and space cooling energy consumption; and to estimate the effects of the socio-economic factors on this consumption in the Canadian residential sector.
          * Estimate the space and domestic hot-water heating energy consumptions in the sector
          * Used for air conditioning set-back controlling, and for optimizing HVAC thermal energy storage in public and office buildings.
          * Chiller plant energy use of a building in a tropical climate; Predict energy savings in equipment retrofit.
          * Internal temperature with easily measurable inputs which include outdoor temperature, solar irradiance, heating valve position and the building indoor temperature.
        * Building energy performance parameters can be estimated by neural networks
        * Predict
          * Estimate the total heat loss coefficient, the total heat capacity and the gain factor which are important for a reliable energy demand forevcast
          * RNN on hourly energy consumption data. Finding the thermal resistance, R, and thermal capacitance, C, for buildings.
          * Evaluate the Coefficient of Performance (COP) of existing rooftop units.
          * Building energy in tropical climates, predicting a weighted energy use index.
        * Data pre-processing technologies
          * Predict 
            * Short-term electricity load with predicted climatic variables; Predicting cooling load.
            * Cooling load profile of the next day, with only single dry-bulb temperature.
            * Building heating loads without considering climatic variables. Just transparency ratio, building orientation and insulation thickness.
            * Online building energy prediction.
            * PCA to reduce the variable dimension before predict annual heating demand.
            * Building energy load prediction. With genetic algorithm for the variable extraction
            * Air-conditioning load.
            * Cooling load.
            * Daily steam load of buildings.
            * Hourly energy loads.
        * Comparisons between neural network and other prediction models
          * NN was very applicable to the annual electricity consumption prediction in manufacturing industries v/s conventional non-linear regression model with (ANOVA)
          * NN can achieve higher prediction performance thatn engineering models in estimating, appliance, lighting and space cooling (ALC) energy consumption and effects of socio-economic factors on this consumptions in the Canadian residential sector
          * NN v/s CDA
            * NN are easier to develop and use
          * NN v/s Elaborate engineering method
            * Both showed high prediction accuracy
            * NN slightly better in short-term prediction
    * ## [[Support Vector Machines]]
      *  Support Vector Machines (SVMs) for building energy analysis. The studies found that SVMs are highly effective in solving non-linear problems, even with small amounts of training data. 
      * They were used to predict monthly and hourly electricity consumption, cooling load, and annual electricity consumption.
      * The studies demonstrated that SVMs perform well in these predictions and are better than other models such as ARIMA, back propagation neural networks, and general regression neural networks. Some research also focused on pre- or post-processing techniques to improve the performance of SVMs, such as reducing 
variables using correlation coefficient and regression gradient or using clustering algorithms and Markov chains.
    * ## Grey models
      * The grey models are used to analyze building energy behavior when there is only incomplete or uncertain data. Little work has been done regarding this model, but studies have been done to apply the grey model to predict building energy behavior.
      * Wang et al. applied the grey model to predict building heat moisture system with high accuracy.
      *  Guo et al. used an improved grey system to predict energy consumption of heat pump water heaters in residential buildings with best interval of four weeks.
      *  Zhou et al. did online prediction of cooling load by integrating two weather prediction modules into a simplified building thermal load model. The results showed improvement in performance when predicted 
weather data is used in the training process.
  * # Discussion and prospects
    * The models have their own advantages in certain cases. Building energy prediction can be done with the help of ANNs and SVMs.
    * The article discusses the various models used to predict building energy consumption, such as engineering models, statistical models, and artificial intelligence models including artificial neural networks (ANNs) and support vector machines (SVMs). Each model has its own advantages and disadvantages, and choosing the best model depends on various factors. The authors suggest that future research should focus on developing more effective and efficient prediction models, refining the models' system-level energy consumption, applying energy prediction to the Building Energy Management System (BEMS), optimizing parameters for accurate prediction, evaluating the influence of each variable on empirical models, and establishing databases to collect precise and sufficient historical consumption data. 
  * # Conclusions
    * The article concludes by noting that while each model is still being developed, the rapid development of artificial intelligence may bring about new and more powerful technologies that could lead to alternatives or even breakthroughs in predicting building energy consumption.