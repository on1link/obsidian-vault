  * # Abstract
    * The abstract should briefly summarize the contents of the paper in 15--250 words.
  * # Introduction
    * One of the world largest issues are climate change, the insasiable need for energy. The first one due to fossil fuels, and greenhouse gases produced by the industry, the second one is due to the growing population and new technologies that demands highers energy needs. One of the solution for both problems and that countries are trying to agreed is the need of change to a electri grid 100\% based on renewables energies.
    * In this context one of the most popular and cost-effective types of renewable energy is wind power. It is a free source, low cost in terms of impĺementation and maintance and many many more. Because of that there is a need of high wind penetration on the system to be realiable the supply on the grind, the main problem with this is that wind is a natural process that have high variability and randomness. In general exists two approach to forecast this penetration: one via calculating the direct power on the wind turbin, and another via forecasting the wind speed and transform it to power energy. This can be posible because of a direct exponential relationship between these two components.
    * To solve this problem many authos has trying to use a variety of models that can be classified in the three main categories: * Phisical models, * Statistical models * Hybrid models.
    * Also the problem of wind speed forecasting can be divided depending of the step ahead we want to predict, this can be translate into: * very short term * short term * medium term * long term.
    * In this paper is proposed a hibryd method that is based attetion mechanism to do the forecasting in a one-step rolling out, the main purpose of this approach is to improve the interpretability of the forecast, learn long term dependencies, and increase the perfomance based on the choosen metrics, and finally study its robustness in the different time scale metion above.
    * The rest of the paper is organized as follows. In Sect. 2 we discuss the theoretical framework, outlining RNN, LSTM, Transformer, and Attention Mechanims. Next Sect. 3 the proposal is described. Sect.4 is for the experimental setting and results, and finally Sect. 5 to conclusions and futuro works.
  * # Theoritical Framework
    * # ARIMA
    * ## [[Recurent Neural Networks]]
      * A recurrent neural network (RNN) is specialized for learning a sequence of values $$ x^{(1)},..., x^{(T)}$$. Unlike traditional neural networks a RNN allows cyclical connections.
      * The Key point is that the recurrent connections allow a 'memory' of previous inputs to persist in the network's internal state, and thereby influence the network output.
      * A useful way to visualize RNNs is to consider the update graph formed by 'unfolding' the network along the input sequence figure[]. Viewing RNNs as unfolded graphs make it easier to generalize to network with more complex update dependencies.
        * $$s_t = f(U x_t + W s_{t-1} + b_{s})$$
        * $$o_t = g(V s_t + b_o)$$
      * RNN's suffers from gradient explosion/vanish problem
    * ## [[LSTM]]
    * ## ((Attention Mechanism))[[Attention Mechanism]]
    * ## ((roYoHMkd_))
  * # Related Work
    * This related work has to be in two sections
    * ## Wind speed forecasting
    * ## Transformer in time series forecasting
  * # Proposal
  * # Experiment and results
  * # Discussion
    * ## Interpretability of attention modules and time series

  * # Appendix A: Problem Definition
  * # Appendix B: More about Transformers
  * # Appendix C: About NAS and Transformers
