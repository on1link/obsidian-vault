  * ## Abstract
    *  Many real-world applications require the prediction of long sequence time-series, such as electricity consumption planning. Long sequence time-series forecasting (LSTF) demands a high prediction capacity of the model, which is the ability to capture precise long-range dependency coupling between output and input efficiently. Recent studies have shown the potential of Transformer to increase the prediction capacity. However, there are several severe issues with Transformer that prevent it from being directly applicable to LSTF, including quadratic time complexity, high memory usage, and inherent limitation of the encoder-decoder architecture. To address these issues, we design an efficient transformer-based model for LSTF, named Informer, with three distinctive characteristics: (i) a ProbSparse self-attention mechanism, which achieves O(L log L) in time complexity and memory usage, and has comparable performance on sequences dependency alignment. (ii) the self-attention distilling highlights dominating attention by halving cascading layer input, and efficiently handles extreme long input sequences. (iii) the generative style decoder, while conceptually simple, predicts the long time-series sequences at one forward operation rather than a step-by-step way, which drastically improves the inference speed of long-sequence predictions. Extensive experiments on four large-scale datasets demonstrate that Informer significantly outperforms existing methods and provides a new solution to the LSTF problem.

  * ![[Roam/Turing/Attachments/imgs/app/Turing/1sZM5ncOX8.png]]
    * Left: The encoder receives massive long sequence inputs (green series). Replace canonical self-attention with the proposed _ProbSparse_ self-attention. The blue trapezoid is the self-attention distillating operation to extract dominating attention, reducing the network size sharply. The layer stacking replicas increase robustness.
    * Right: The decoder receives long sequences inputs, pads the targets elements into zero, measures the weighted attention composition of the feature map, and instantly predicts output elements (orange series) in a generative style.
  * Their present that Vainnila Transformer [[Vaswani, A.2017 Attention is all you need]] have three main issues
    * **The quadratic computation of self-attention**
      * Their mention some prior work improving the efficiency of self-attention.
        * Using a heuristic methods and reduce the complexity of self-attention to $$O (L \log L)$$
        * Sparse Transformer [[Child, R.2019 Generating long sequences with sparse transformers]]
        * LogSparse Transformer [[Li, S.2019 Enhancing the Locality and Breaking the Memory Bottleneck of Transformer on Time Series Forecasting]]
        * Longformer ??
    * **The memory bottleneck in stacking layers for long inputs**
    * **The speed plunge in predicting long outputs**
  * One of the big difference between this papers and other prior work is the form to extract the relevant dot-product from the self-attention layer using de DL divergence  comparing the long tail distrinbution in self-attention feature map, i.e.  a few dot-products pairs contribute to the major attention and others can be ignored.
    * ![[Roam/Turing/Attachments/imgs/app/Turing/7i8-_-u9Ko.png]]
  * # References
  * [[Hochreiter, S.1997 Long short-term memory]]
  * [[Bahdanau, D.2014 Neural machine translation by jointly learning to align and translate]]
  * [[Vaswani, A.2017 Attention is all you need]]
  * [[Li, S.2019 Enhancing the Locality and Breaking the Memory Bottleneck of Transformer on Time Series Forecasting]]
  * [[Song2018 Attend and Diagnose Clinical Time Series Analysis Using Attention Models]]
  * [[Child, R2019 Generating long sequences with sparse transformers]]