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
