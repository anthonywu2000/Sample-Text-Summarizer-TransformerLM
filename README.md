# Text Summarizer TransformerLM
An attempt to build a decoder-only Transformer language model that summarizes text from news articles. The model is build from using Google Trax NLP API. Graphically, the model is built based on this architecture, though there is no encoder-decoder attention in our model.

<img width="617" alt="Screen Shot 2023-09-03 at 1 48 39 PM" src="https://github.com/anthonywu2000/Sample-Text-Summarizer-TransformerLM/assets/52024770/e5d9fc8f-fc64-436e-97d9-e8edf44df694">

The use of multi-head attention is to capture the relationship of words/texts based on different dimensions and linear transformations. In this model, the data is fed in this format:
`ARTICLE<EOS>SUMMARY<EOS><pad>....`. The feed forward block of the decoder block is used to normalize the outputs from the multi-head attention and change dimensions in order for the output to be used for generating word probabilities from the LogSoftmax function via another dense layer. The feed forward block is created with two dense layers with dropout, and a ReLU activation function. 

Additionally, the positional encoding is used to give information to the model about the relative word positions within the sequence.

<img width="527" alt="Screen Shot 2023-09-03 at 4 57 22 PM" src="https://github.com/anthonywu2000/Sample-Text-Summarizer-TransformerLM/assets/52024770/d0a7f929-0e0f-46ff-b80b-bf1cd90da901">

The model is also implemented with a greedy decoder at the end, specifying the most probable word that comes next in the sequence after each produced generated word.
Metrics of this model include cross-entropy loss and accuracy. 

<img width="457" alt="Screen Shot 2023-09-03 at 1 53 49 PM" src="https://github.com/anthonywu2000/Sample-Text-Summarizer-TransformerLM/assets/52024770/6873e828-d7cb-4a54-ba29-ad1f9043cf74">


