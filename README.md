# Predicting the Total Number of Claps of a Medium Blog Post

The project aims to predict the number of claps for given Medium blog posts. The training data set consists of 279.577 entries and contains 50 different variables representing the meta data retrieved from the scrapped blog posts. All data was scrapped at November 04, 2018. The testing data set has only 8 different variables and 514 observations. <br>

To build a model that predicts the number of claps of a given Medium blog posts, I focused mainly on the texts of the articles. In order to catch the semantic as well as syntactic relationship between words, I used GloVe (Wikipedia 2014 + Gigaword 5) as a pre-trained model as well as self-trained word2vec embeddings (Skip-gram, Cbow) -- each with 150 and 300 dimensions. As an evaluation model on which embedding to use for the final prediction, a non-trainable GRU with only 10 epochs was used. SPOILER: the word2vec model Cbow with 300 dimension performed best.

For the prediction, an elastic net was applied as a baseline model. Additionally, a MLP, GRU and Bi-directional GRU were trained and used for the prediction of the total number of claps. The MSE is used as an evaluation metric.

All code was written in Python within a jupyter notebook environment and colab.

**Note**: Unfortunately, the chair of information systems at the Humboldt university prohibits the sharing of the data sets. In case you are interested in working with them, please contact the Prof. Lessmann.

## Organization

__Author:__ Anna Franziska Bothe <br>
__Institute:__ Humboldt University Berlin, Chair of Information Systems <br>
__Course__: Advanced Data Analytics for Management Support <br>
__Semester:__ SS 2020 <br>


## Content

```
.
├── ADAMS_NLP_SS20_AFBothe.ipynb  # final notebook containing code and all comments
├── README.md                     # this readme file
├── requirements.txt              # contains all used packages
├── setup.txt                     # describes execution of pipeline in detail, s. note on data sets above

```







