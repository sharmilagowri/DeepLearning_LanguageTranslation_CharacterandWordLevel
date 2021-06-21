# DeepLearning_LanguageTranslation_CharacterandWordLevel

Translating English into Marati Language. Used LSTM's Seq to Seq model which follows encoder-decoder architecture. 

Sequence-to-sequence learning (Seq2Seq) is about training models to convert sequences from one domain (e.g. sentences in English) to sequences in another domain (e.g. the same sentences translated to French).
Encoder: Takes input sentence and maps to meaning vector (h,c) which understands the input and encodes to the vector
Decoder: We feed meaning vector to the decoder. It decodes the English input and translate to the Marathi words
We use LSTM, we take hidden state and cell state from LSTM (h,c) and feed (h,c) and 'start' to the decoder. Initially it gives some random output but after back propagation, it corrects the error at different time stamps

In this project, language translation is done using Character Level and Word Level

The major drawback of encoder-decoder model in sequence to sequence recurrent neural network is that it can only work on short sequences. It is difficult for the encoder model to memorize long sequences and convert it into a fixed-length vector. Moreover, the decoder receives only one information that is the last encoder hidden state. Hence it's difficult for the decoder to summarize large input sequence at once

Now, this is where the concept of ‘Attention Mechanism’ comes. The major intuition about this is that it predicts the next word by concentrating on a few relevant parts of the sequence rather than looking on the entire sequence.

Instead of a simple encoder-decoder architecture, we used Attention Mechanism. Keras does not officially support attention layer. So, we can either implement our own attention layer or use a third-party implementation. For now, we used a third party attention mechanism. we also uploaded 'attention.py' file to the local. This attention is an implementation of ‘Bahdanau Attention’ 

Got the dataset from http://www.manythings.org/anki/




