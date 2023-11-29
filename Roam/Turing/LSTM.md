  * LSTM [[Hochreiter, S.1997 Long short-term memory]] are based on the idea of creating paths without the above mention gradient descent problem. The main goal of a LSTM is to automatically decide when remember and when forget the information.
  * A LSTM network contains a set of LSTM blocks instead of, regular network units. A LSTM block contains gates that determine when the input is significant enough to remember from the input value, when it should continue to remember or forget the value from the previous internal cell state, and when it should output the value. These gates are called input, forget and output gates, and control the internal information flow of the network.
    $$f_t = \sigma(W_f x_t + U_f s_{t-1} + b_f)$$
    $$i_t = \sigma(W_i x_t + U_i s_{t-1} + b_i)$$
    $$s_t = f_t * s_{t-1} + i_t * tanh(W_s x_t + U_s s_{t-1} + b_s)$$
    $$y_t = \sigma(W_y x_t + U_y s_{t-1} + b_{y})$$
    $$o_t = tanh (s_t) * y_t$$