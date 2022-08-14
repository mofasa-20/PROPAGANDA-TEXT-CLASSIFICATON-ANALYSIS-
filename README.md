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
## Introduction
* The landscape of news outlets is wide: from supposedly neutral to clearly biased.  When reading a news article, every reader should be aware that, at least to some extent, it inevitably reflects the bias of both the author and the news outlet where the article is published. However, it is difficult to identify exactly what the bias is. It could be that the author himself may not be conscious about his own bias. On the other hand, it could be that the article is part of the author’s agenda to persuade readers about something on a specific topic. The latter situation represents propaganda. According to the now classical work from the Institute for Propaganda Analysis [1], propaganda can be defined as follows:

Definition 1: Propaganda is expression of opinion or action by individuals or groups deliberately designed to influence opinions or actions of other individuals or groups with reference to predetermined ends.

## Features

* The corpus contains 52k articles from 100+ news outlets. Each article is
labeled as either “propagandistic” (positive class) or “non-propagandistic”
(negative class). The labeling was done indirectly using a technique known as
distant supervision, i.e. an article is considered propagandistic if it comes
from a news outlet that has been labeled as propagandistic by human annotators.

## About Data

* The dataset is taken from the given source [data](https://zenodo.org/record/3271522#.YgK9ie5BzDI).
We provide the corpus in three tsv files, including training, development, and
testing partitions.

The data is tab-separated. Each line represents one article, with the following
information:

1. article_text: the text of the article retrieved via newspaper3k package.
2. event_location: the geographical location - collected from GDELT.
3. average_tone: measures the impact of the event - collected from GDELT
4. article_date: article's publish date - collected from GDELT.
5. article_ID: GDELT ID , unique among the dataset's articles.
6. article_URL: the direct URL for the published article in its source website.
7. MBFC_factuality_label: factuality label for the source from MBFC
8. article_URL
9. MBFC_factuality_label   
10. URL_to_MBFC_page        
11. source_name     
12. MBFC_notes_about_source
13. MBFC_bias_label
14. source_URL
15. propaganda_label

## Data Info:
![Data Info](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/Data%20Info.JPG)

## Optimal Column Selection.
•	The above training dataset has total of 15 columns/features.

•	The most important features out of 15 are the input text ("text"), headline ("URL.1"), and the output label (propaganda_label).

•	We I am removing the rest columns and keeping the above mention one.

## Target Label Analysis
![t1](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/Target%20Label%20Analysis.JPG)
![t2](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/Target%20Label%20Analysis2.JPG)
![t3](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/Target%20Label%20Analysis3.JPG)
![t4](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/Target%20Label%20Analysis4.JPG)

Observations:

"-1" represents no propaganda, and "1" represents yes propaganda.

The class is highly imbalance as only 11.2% of text consists of propaganda yes.


## n-gram Analysis
![n1](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/ng1.JPG)
![n2](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/ng2.JPG)

## bi-gram Analysis
![b1](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/bg1.JPG)
![b2](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/bg2.JPG)

## tri-gram Analysis
![tr1](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/tg1.JPG)
![tr2](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/tg2.JPG)

## Word Cloud
![wc1](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/wc1.JPG)
![wc2](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/wc2.JPG)

## Naive bayes classifier - count vectorizer
![nbcv](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/nbcv.JPG)

## Naive bayes classifier - tfidf vectorizer
![nbcv](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/nbtv.JPG)

## Logistic Regression - count vectorizer
![lrcv](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/lrcv.JPG)

## Logistic Regression - tfidf vectorizer
![lrtv](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/lrtv.JPG)

## Support Vector Machine - count vectorizer
![svmcv](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/svmcv.JPG)


## Support Vector Machine - tfidf vectorizer
![svmtv](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/svm%20tdf.JPG)


##  LSTM model Plots, Classification Report & Prediction
![plot](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/lstm1.JPG)

![cr](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/lstmcr.JPG)

![pred](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/lstmcm.JPG)


## Attention LSTM Model Plots, Classification Report & Prediction 
![plot](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/alstm1.JPG)

![cr](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/alstmcr.JPG)

![pred](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/alstmcm.JPG)



## Documentation:

[Report](https://github.com/mofasa-20/PROPAGANDA-TEXT-CLASSIFICATON-ANALYSIS-/blob/main/Report/Project%20Report%20for%20GitHub.pdf)

## References:
[ALPAC- Automatic Language Processing Advisory Committee](https://en.wikipedia.org/wiki/ALPAC)

[Ba, M. L., Berti-Equille, L., Shah, K., & Hammady, H. M. (2016). VERA: A platform for veracity estimation over web data. Proceedings of the 25th International Conference Companion on World Wide WebWWW ’16159–162 Montréal, Québec, Canada Baeza-Yates, R. (2018).](https://dl.acm.org/doi/10.1145/2872518.2890536)

[Recursive hetero-associative memories for translation](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.43.1968&rep=rep1&type=pdf)

[Bias on the web. Communications of the ACM, 61(6), 54–61.](https://dl.acm.org/doi/10.1145/2872518.2890536)

[Recurrent Continuous Translation Models](https://aclanthology.org/D13-1176/)

[Baly, R., Karadzhov, G., Alexandrov, D., Glass, J., & Nakov, P. (2018). Predicting factuality of reporting and bias of news media sources. Proceedings of the 2018 Conference on Empirical Methods in nAtural Language ProcessingEMNLP ’183528–3539.](https://aclanthology.org/D18-1389/)

[Sequence to Sequence Learning with Neural Networks](https://proceedings.neurips.cc/paper/2014/file/a14ac55a4f27472c5d894ec1c3c743d2-Paper.pdf)

[Barrón-Cedeño, A., Da San Martino, G., Zhang, Y., Ali, A., & Dalvi, F. (2018). Qlusty: Quick and dirty generation of event videos from written media coverage. Proceedings of the Second International Workshop on Recent Trends in News Information Retrieval27–32 Grenoble, France](https://www.scopus.com/home.uri)

[Neural Computation - Long Short-Term Memory - LSTM ](https://direct.mit.edu/neco/article-abstract/9/8/1735/6109/Long-Short-Term-Memory?redirectedFrom=fulltext)

[Bazerman, C. (2010). The informed writer: Using sources in the disciplines. Fort Collins, CO, USA: The WAC Clearinghouse.](https://scholar.google.com/scholar_lookup?title=The%20informed%20writer%3A%20Using%20sources%20in%20the%20disciplines&author=C.%20Bazerman&publication_year=2010)
[ALPAC- Automatic Language Processing Advisory Committee](https://en.wikipedia.org/wiki/ALPAC)

[JANUS: a speech-to-speech translation system using connectionist and symbolic processing Strategies](https://isl.anthropomatik.kit.edu/downloads/CP_1991_JANUS-_A_Speech-to-Speech_Translation_System_Using_Connectionist_and_Symbolic_Processing_Strategies(1).pdf)

[Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473#)

[Learning Phrase Representations using RNN Encoder-Decoder for Statistical Machine Translation](https://arxiv.org/abs/1406.1078)

[Convolutional Sequence to Sequence Learning](https://arxiv.org/abs/1705.03122)

[Bird, S., Loper, E., & Klein, E. (2009). Natural language processing with python. O’Reilly Media Inc.](https://books.google.ca/books?hl=en&lr=&id=KGIbfiiP1i4C&oi=fnd&pg=PR5&ots=Y4EfA1OBH5&sig=EHdt_ZsUX0AWJ4CzvD5QPFhCQ0s&redir_esc=y#v=onepage&q&f=false)

[Brill, A. M. (2001). Online journalists embrace new marketing function. Newspaper Research Journal, 22(2), 28.](https://journals.sagepub.com/doi/10.1177/073953290102200203)

[Canini, K. R., Suh, B., & Pirolli, P. L. (2011). Finding credible information sources in social networks based on content and social structure. Proceedings of the IEEE International Conference on Privacy, Security, Risk, and Trust, and the IEEE International Conference on Social ComputingSocialCom/PASSAT ’111–8 Boston, Massachusetts, USA](https://ieeexplore.ieee.org/document/6113088)

[Castillo, C., Mendoza, M., & Poblete, B. (2011). Information credibility on Twitter. Proceedings of the 20th International Conference on World Wide WebWWWZ’11675–684
Hyderabad, India](https://dl.acm.org/doi/10.1145/1963405.1963500)

[Chen, C., Wu, K., Srinivasan, V., & Zhang, X. (2013). Battling the Internet Water Army: Detection of hidden paid posters. Proceedings of the 2013 IEEE/ACM International Conference on Advances in Social Networks Analysis and MiningASONAM ’13116–120 Niagara, Ontario, Canada](https://dl.acm.org/doi/10.1145/2492517.2492637)

[Conserva, H. (2003). Propaganda techniques. United States: AuthorHouse.](https://books.google.ca/books?hl=en&lr=&id=5ip9vVZ-H4sC&oi=fnd&pg=PA2&ots=xjzMk6Fg7v&sig=6sdQuYJQOp1X0EkLKLWG52aHx6Q&redir_esc=y#v=onepage&q&f=false)

[Cristianini, N., & Shawe-Taylor, J. (2000). An Introduction to Support Vector Machines and other kernel-based learning methods. Cambridge University Press.](https://books.google.ca/books?hl=en&lr=&id=_PXJn_cxv0AC&oi=fnd&pg=PR9&ots=xTSd6B3qYf&sig=mOQjOmF1DZ3-G4lFbsGVX9lWu6o&redir_esc=y#v=onepage&q&f=false)

[Derczynski, L., Bontcheva, K., Liakata, M., Procter, R., Wong Sak Hoi, G., & Zubiaga, A. (2017). SemEval-2017 Task 8: RumourEval: Determining rumour veracity and
support for rumours. Proceedings of the 11th International Workshop on Semantic EvaluationSemEval ’1760–67 Vancouver, Canada](https://arxiv.org/abs/1704.05972)

[Ellul, J. (1965). Propaganda: The formation of men’s attitudes. United States: Vintage Books.](https://d1wqtxts1xzle7.cloudfront.net/52794526/Propaganda_-The_Formation_Of_Mens_Attitudes_By_Jacques_Ellul-with-cover-page-v2.pdf?Expires=1660436647&Signature=giCcyh1FxWOySvDCygdhyJVUMeN-GTKzwCeE5TeW7BSb-~T9Pi9e27zX6pZS7s~m6wt~a-G3bMWStcvrQtVxCXbVL1qqDlWFgPlx~X86Q2DJwqm~FPTZr7X8jyWMIiGdpU5-ailPSpYOLMf-nuZFm19KnNJfvuZ~bwaB5IONNENW5xPjFdk48QePkgSvYQByT72RBS2g6Ngxyc5X3U~cEVilyoVYW-7eUDJ5RqbjhbiNdEslT63k9Ui1W6Wha4E4XBuDGjV5cihOQ62k0wbZ5wpuDUYn~xzMYaKj3PiemXthYJv5a2jKQbJoS4vM~pRwCwVC4kyf12eHZkoz2PuQCw__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)

[Ester, M., Kriegel, H.-P., Sander, J., & Xu, X. (1996). A density-based algorithm for discovering clusters in large spatial databases with noise. Proceedings of the Second International Conference on Knowledge Discovery and Data MiningKDD ’96226–231 Portland, OR, USA](https://www.aaai.org/Papers/KDD/1996/KDD96-037.pdf?source=post_page)

[Graham, J., Haidt, J., & Nosek, B. A. (2009). Liberals and conservatives rely on different sets of moral foundations. Journal of Personality and Social Psychology, 96(5),1029.](https://psycnet.apa.org/doiLanding?doi=10.1037%2Fa0015141)

[Gunning, R. (1968). The technique of clear writing. McGraw-Hill.](https://agris.fao.org/agris-search/search.do?recordID=US201300348129)

[Hardalov, M., Koychev, I., & Nakov, P. (2016). In search of credible news. Proceedings of the 17th International Conference on Artificial Intelligence: Methodology, systems, and applicationsAIMSA ’16172–180 Varna, Bulgaria](https://link.springer.com/chapter/10.1007/978-3-319-44748-3_17)

[Hooper, J. (1975). On assertive predicates. 4. Academic Press, New York.](https://onlinelibrary.wiley.com/doi/10.1002/9781118611463.wbielsi003)

[Horne, B. D., & Adal, S. (2017). This just in: Fake news packs a lot in title, uses simpler, repetitive content in text body, more similar to satire than real news. Proceedings of the international workshop on news and public opinion at ICWSM Montreal, Canada](https://www.aaai.org/ocs/index.php/ICWSM/ICWSM17/paper/view/15772/14898)

[How to Detect Propaganda (1938). In Institute for Propaganda Analysis (Ed.). Propaganda analysis. volume i of the publications of the institute for propaganda analysis (pp. 210–218). New York, NY](https://www.scopus.com/home.uri)

[Jaccard, P. (1901). Étude comparative de la distribution florale dans une portion des Alpes et des Jura. Bulletin del la Société Vaudoise des Sciences Naturelles, 37,
547–579.](https://cir.nii.ac.jp/crid/1570009750546179712)

[Japkowicz, N., & Shah, M. (2011). Evaluating learning algorithms: A classification perspective. New York, NY: Cambridge University Press.](https://books.google.ca/books?hl=en&lr=&id=VoWIIOKVzR4C&oi=fnd&pg=PR7&ots=5y80VGQzKF&sig=-jl5r6f6JA0_VfZICyPSXLfbR2o&redir_esc=y#v=onepage&q&f=false)

[Translation Engines](https://www.academia.edu/5965803/Translation_Engines_Techniques_for_Machine_Translation_Arturo_Trujillo_Springer_Verlag_Applied_Computing_Heidelberg_1999_ISBN_1_85233_057_0111)

[Potthast, M., Kiesel, J., Reinartz, K., Bevendorff, J., & Stein, B. (2018). A stylometric inquiry into hyperpartisan and fake news. Proceedings of the 56th annual meeting of the Association for Computational LinguisticsACL ’18231–240 Melbourne, Australia](https://aclanthology.org/P18-1022/)

[Rashkin, H., Choi, E., Jang, J. Y., Volkova, S., & Choi, Y. (2017). Truth of varying shades: Analyzing language in fake news and political fact-checking. Proceedings of the 2017 Conference on Empirical Methods in Natural Language ProcessingEMNLP ’172931–2937 Copenhagen, Denmark](https://aclanthology.org/D17-1317/)

[Shu, K., Sliva, A., Wang, S., Tang, J., & Liu, H. (2017). Fake news detection on social media: A data mining perspective. SIGKDD Explorations Newsletters, 19(1), 22–36.](https://dl.acm.org/doi/10.1145/3137597.3137600)

[Sproule, J. M. (2001). Authorship and origins of the seven propaganda devices: A research note. Rhetoric & Public Affairs,, 4(1), 135–143.](https://muse.jhu.edu/article/29876)

[Stamatatos, E. (2009). A survey of modern authorship attribution methods. Journal of the American Society for Information Science and Technology, 60(3), 538–556.](https://onlinelibrary.wiley.com/doi/10.1002/asi.21001)

[Thorne, J., & Vlachos, A. (2018). Automated fact checking: Task formulations, methods and future directions. Proceedings of the 27th International Conference on
Computational LinguisticsCOLING ’183346–3359 Santa Fe, NM, USA](https://arxiv.org/abs/1806.07687)

[Thorne, J., Vlachos, A., Christodoulopoulos, C., & Mittal, A. (2018). FEVER: A large-scale dataset for fact extraction and VERification. Proceedings of the 2018 conference of the North American chapter of the Association for Computational Linguistics: Human language technologiesNAACL-HLT ’18809–819 New Orleans, LA, USA](https://aclanthology.org/N18-1074/)

[Vosoughi, S., Roy, D., & Aral, S. (2018). The spread of true and false news online. Science, 359(6380), 1146–1151.](https://www.science.org/doi/10.1126/science.aap9559)

[Wilson, T., Wiebe, J., & Hoffmann, P. (2005). Recognizing contextual polarity in phrase-level sentiment analysis. Proceedings of the Conference on Human Language
Technology and Empirical Methods in Natural Language ProcessingNAACL-HLT ’05347–354 Vancouver, Canada](https://dl.acm.org/doi/10.3115/1220575.1220619)

[Zubiaga, A., Liakata, M., Procter, R., Wong Sak Hoi, G., & Tolmie, P. (2016). Analysing how people orient to and spread rumours in social media by looking at
conversational threads. PLoS ONE, 11(3), 1–29.](https://books.google.ca/books?hl=en&lr=&id=B9VkAwAAQBAJ&oi=fnd&pg=PR9&ots=v6YBL3jtI5&sig=-cmoSANnyRrwbL7loPNBnMPubjw&redir_esc=y#v=onepage&q&f=false)


## Remark:
Path - Path is hardcoded in the coding so please change the path before you run the code.


