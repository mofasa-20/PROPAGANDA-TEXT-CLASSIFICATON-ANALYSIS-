# PROPAGANDA TEXT CLASSIFICATON ANALYSIS: NEWS BASED ON THEIR PROPAGANDISTIC CONTENTS
[![Python](https://warehouse-camo.ingress.cmh1.psfhosted.org/582ab2eba9d0e0f4acbea2fd883f604349908147/68747470733a2f2f696d672e736869656c64732e696f2f707970692f707976657273696f6e732f74656e736f72666c6f772e7376673f7374796c653d706c6173746963)](https://pypi.org/project/tensorflow/2.8.0/)
[![PyPI](https://warehouse-camo.ingress.cmh1.psfhosted.org/76cd0764983d405a55b91b028b8ea467797f1816/68747470733a2f2f62616467652e667572792e696f2f70792f74656e736f72666c6f772e737667)](https://pypi.org/project/tensorflow/2.8.0/)
[![tqdm](https://warehouse-camo.ingress.cmh1.psfhosted.org/6c7e16a4732b3e24d08c464d155bde3b89d95f80/68747470733a2f2f696d672e736869656c64732e696f2f707970692f707976657273696f6e732f7471646d2e7376673f6c6f676f3d707974686f6e266c6f676f436f6c6f723d7768697465)](https://pypi.org/project/tqdm/4.64.0/)


<p align="justify">
    “Propaganda is a mechanism to influence public opinion, which is inherently present in extremely biased and fake news.” If a Celebrity/famous personality has given his/her personal opinion about any upcoming or occurred event organized by a government which is disliked by political parties, organizations, or any individuals then those political parties or individuals can come up with an extreme bias by manipulating original opinion. Here, I propose a model to automatically assess the level of propagandistic content in an article based on different representations, from writing style and certain keywords. I experiment thoroughly with different variations of such a model on a new publicly available corpus, and I show that character n-grams and other style features outperform existing alternatives to identify propaganda based on word n-grams. I make sure that the test data comes from news sources that were unseen on training, thus penalizing learning algorithms that model the news sources used at training time as opposed to solving the actual task. This allows users to quickly explore different perspectives of the same story, and it enables investigative journalists to dig further into how different media use stories and propaganda to pursue their agenda.
</p>

## Packages

Below are the python packages version details. Incase to install any package the easiet way to do it using "pip:"

```bash
python == 3.7.13
re == 2.2.1       
numpy == 1.21.6       
pandas == 1.3.5        
nltk == 3.2.5
sklearn == 1.0.2
matplotlib == 3.2.2
tqdm == 4.64.0
seaborn == 0.11.2
tensorflow == 2.8.0
keras == 2.8.0

Installation Example:

pip install tensorflow==2.8.0
```

## Features

* State-of-the-art models implemented using Encoder-Decoder, and Attention mechanism.
* Utilities to evaluate models performance and compare their accuracy using BLEU score and log loss
* Building blocks to define custom models and quickly experiment

## About Data

* The dataset is taken from the given source [data](http://www.manythings.org/anki/).
* It is a "Tab-delimited Bilingual Sentence Pairs" and present from one natural language to another natural language.
* I have selected French to English sentence pair for machine translation.



## Documentation:

[Report](https://github.com/mofasa-20/dd-Techniques/blob/main/Report/MRP_Project_Report_Mohammed_Abdul_Faheem.pdf)

## Other resources:
[ALPAC- Automatic Language Processing Advisory Committee](https://en.wikipedia.org/wiki/ALPAC)


[Recursive hetero-associative memories for translation](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.43.1968&rep=rep1&type=pdf)

[Translation Engines](https://www.academia.edu/5965803/Translation_Engines_Techniques_for_Machine_Translation_Arturo_Trujillo_Springer_Verlag_Applied_Computing_Heidelberg_1999_ISBN_1_85233_057_0111)

[JANUS: a speech-to-speech translation system using connectionist and symbolic processing Strategies](https://isl.anthropomatik.kit.edu/downloads/CP_1991_JANUS-_A_Speech-to-Speech_Translation_System_Using_Connectionist_and_Symbolic_Processing_Strategies(1).pdf)

[Recurrent Continuous Translation Models](https://aclanthology.org/D13-1176/)

[Sequence to Sequence Learning with Neural Networks](https://proceedings.neurips.cc/paper/2014/file/a14ac55a4f27472c5d894ec1c3c743d2-Paper.pdf)

[Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473#)

[Neural Computation - Long Short-Term Memory - LSTM ](https://direct.mit.edu/neco/article-abstract/9/8/1735/6109/Long-Short-Term-Memory?redirectedFrom=fulltext)

[Learning Phrase Representations using RNN Encoder-Decoder for Statistical Machine Translation](https://arxiv.org/abs/1406.1078)

[Convolutional Sequence to Sequence Learning](https://arxiv.org/abs/1705.03122)


## Remark:
Path - Path is hardcoded in the coding so please change the path before you run the code.


