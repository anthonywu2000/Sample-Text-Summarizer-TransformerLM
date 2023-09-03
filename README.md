# Sample-Text-Summarizer-TransformerLM
An attempt to build a decoder-only Transformer language model that summarizes text from news articles. The model is build from Google Trax NLP API. Graphically, the model is built based on this architecture, though there is no encoder-decoder attention in our model.

<img width="617" alt="Screen Shot 2023-09-03 at 1 48 39 PM" src="https://github.com/anthonywu2000/Sample-Text-Summarizer-TransformerLM/assets/52024770/e5d9fc8f-fc64-436e-97d9-e8edf44df694">

The use of multi-head attention is to capture the relationship of words/texts based on different dimensions and linear transformations. In this model, the data is fed in this format"
`ARTICLE<EOS>SUMMARY<EOS><pad>....`. The model is also implemented with a greedy decoder at the end, specifying the most probable word that comes next in the sequence after each produced generated word.
Metrics of this model include cross-entropy loss and accuracy. 

<img width="457" alt="Screen Shot 2023-09-03 at 1 53 49 PM" src="https://github.com/anthonywu2000/Sample-Text-Summarizer-TransformerLM/assets/52024770/6873e828-d7cb-4a54-ba29-ad1f9043cf74">

