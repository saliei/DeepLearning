> *LSTM* networks.

* Notes:
    
    - Recurrent neural networks have loops in nodes, allowing information to persist.
    
    - RNNs shortcomings are persisting information over a long history. They are fundamentally 
        unable to learn relevant parameters.
    - LSTM networks (LSTMs) are a special kind of RNN, capable of learning long-term dependence.
    
    - The repeating module in an LSTM contains four interacting layers (vs 1 in standard RNN).
        <img src="assets/LSTM3-chain.png" style="display:block;margin-left:auto; margin-right:auto; width:60%">
    
    - The horizontal line running through the top of the cells is the cell state, it runs 
        straight down the entire chain, with only minor linear interactions through gates 
        (e.g. the sigmoid function and the pointwise operation).
    
    - The first sigmoid layer is the "forget gate layer", information that need to be thrown away.
        <img src="assets/LSTM3-focus-f.png" style="display:block;margin-left:auto; margin-right:auto; width:75%">
    
    - Deciding what information to keep. This has two layers. A sigmoid layer, called "input gate layer" 
        decides which values we'll update. Next a tanh layer creates a vector of new values that could 
        be added to the cell state.
        <img src="assets/LSTM3-focus-i.png" style="display:block;margin-left:auto; margin-right:auto; width:75%">
    
    - Updating the old cell state. The first part of the equation of the figure, is forgetting  things we decided to 
        forget earlier. The second part is the new candidate values, scaled by how much we decided to update each 
        state values.
        <img src="assets/LSTM3-focus-C.png" style="display:block;margin-left:auto; margin-right:auto; width:75%">
    
    - Deciding the output. First we run a sigmoid layer which decides what parts if the cell state we're going to 
        output. Then we put the cell state through tanh (to push the values to be between -1, and 1) and multiply 
        it by the output of the sigmoid gate, so that we only output the parts we decide to.
        <img src="assets/LSTM3-focus-o.png" style="display:block;margin-left:auto; margin-right:auto; width:75%">


---
* References:
    - [Understanding LSTMs](http://colah.github.io/posts/2015-08-Understanding-LSTMs/)
