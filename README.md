### Encoder and Decoder diagram:

<img src= files/transformer.png  width = "693" height = "492" alt="centered image">

### Abstractive Summarization with Transformers:

<img src= files/abstractivesum.jpg  width = "300" height = "130">

Abstractive summarization is the technique of generating a summary of a text from its main ideas, not by copying verbatim most salient sentences from text. There have been many different algorithms and methods for performing this task including the use of RNNs or the newer networks: Transformers. 

### Dataset:

https://www.kaggle.com/shashichander009/inshorts-news-data

Inshorts is a news service that provides short summaries of news from around the web. This dataset contains headlines and summary of news items along with its source. This dataset includes 55k news and their summaries that I have used as inputs and labels of the model. You can use bigger datasets for better results and more generalization.

### Model settings:

The Encoder block: 1- multi-headed attention (mha) layer, dropout layer and layer normalization 2- a feed foward network (ffn), dropout layer and layer normalization
and the Decoder blobk:  the same blocks as the Encoder except that it contains 2 blocks of mha (multi-headed attention layer, dropout layer and layer normalization  ) x 2 and then, the ffn. Both the Encoder and Decoder have 4 of mentioned blocks. Drop out rate is 0.1 and the batch size is 64. The model is trained on a GTX-1070Ti, each epoch took about 40 seconds.

### Examples of result:

**News text** : a tenminute video traces  us presidential elections in order to provide a historical insight into the event the video discusses the  elections held less than a year after the assassination of the th us president john f kennedy further detailing the history it describes the  elections wherein barack obama was voted as the th us president

**model prediction** : video explains the us elections

===

**News text** : brazilian police on wednesday arrested the head of the european olympic committees patrick hickey in rio de janeiro over illegal sales of olympic tickets police said hickey and at least six others are accused of illegally passing on tickets for the games to be sold on at extortionate prices hickey was taken to hospital after his arrest

**model prediction** : brazil police arrests rio olympics officials


### Tutorials on the Transformers:

* https://towardsdatascience.com/transformers-explained-65454c0f3fa7
* http://jalammar.github.io/illustrated-transformer/
* https://www.youtube.com/watch?v=TQQlZhbC5ps
