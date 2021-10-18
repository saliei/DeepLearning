> *LSTM* networks.

* Notes:
    - Recurrent neural networks have loops in nodes, allowing information to persist.
    - RNNs shortcomings are persisting information over a long history. They are fundamentally 
        unable to learn relevant parameters.
    - LSTM netwoeks (LSTMs) are a special kind of RNN, capable of learning long-term dependence.
    - The repeating module in an LSTM contains four interacting layers (vs 1 in standard RNN).
        <img src="assets/LSTM3-chain.png" style="display:block;margin-left:auto; margin-right:auto; width:50%">

---
* Resources:
    - [Understanding LSTMs](http://colah.github.io/posts/2015-08-Understanding-LSTMs/)
