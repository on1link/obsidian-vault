A recurrent neural network (RNN) is specialized neural network for learning a sequence of values $x^{(1)},..., x^{(T)}$. Unlike traditional neural networks a RNN allows cyclical connections.

The key point is that the recurrent connections allows a 'memory' of previous inputs to persist in the network's internal state, and thereby influence the network output.
A useful way to visualize RNNs is to consider the update graph formed by 'unfolding' the network along the input sequence figure (missing figures). Viewing RNNs as unfolded graphs make it easier to generalize to network with more complex update dependencies. $$s_t = f(U x_t + W s_{t-1} + b_{s})$$, $$o_t = g(V s_t + b_o)$$

RNNs suffers from gradient explosion/vanish problem.
