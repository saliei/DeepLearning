> *seq2seq* models.

* Notes:

    - Neural Machine Translation (NMT) one of the first testbeds of *seq2seq* models.

    - NMT mimics the behaviour of understanding (encoding) a given sentence and then translating (decoding). 
        In another word a **Encoder-Decoder** architecture.

    - Recurrent Neural Network (RNN) is a natural choice for sequential data, used by most NMT models. However it 
        could be uni or bidirectional, single or multi-layer, vanilla or a Long Short-term Memory (LSTM) RNN.

    - This note/tutorial which is based on tensorflow's nmt repository (reference #1), uses a deep multi-layer RNN 
        which is unidirectional and uses LSTM as a recurrent unit. At a high level, the NMT model consists of two 
        recurrent neural networks: the *encoder* RNN simply consumes the input source words without making any prediction; 
        the *decoder* processes the target sentence while predicting the next words.
        <img src="assets/seq2seq.jpg" style="display:block;margin-left:auto; margin-right:auto; width:75%">

---
* Resources:
    1. [Tensorflow NMT](https://github.com/tensorflow/nmt)
    2. [Understanding LSTMs](http://colah.github.io/posts/2015-08-Understanding-LSTMs/)

