
# Gender Bias in Word Embeddings Trained on Movie Review Corpora


Embeddings are numerical representations of words. Embeddings of words with similar semantic meanings are associated closely to each other, since they are likely to appear together in natural language. However, word embeddings can inherit linguistic biases. For example, if the gender stereotypes exist in the corpus used to train or derive the embeddings, then it is natural that embeddings also exhibit the bias.

## Findings and Graphics

In [Figure 1](https://github.com/user-attachments/assets/e3fc8e81-4f4e-437c-98b7-35cbc3c25633), I investigate the association strength, also known as embedding bias, between gender and 5 manually selected classes of target words in 3 distinct word embedding space derived from 3 distinct text corpora:
- Word embeddings derived from the Corpus 1, i.e. reviews on the movies “Tiny Times 1.0” (2013) or “Tiny Times 3.0” (2014).
- Word embeddings derived from the Corpus 2, i.e. reviews on the movie “La La Land” (2016).
- Pre-trained [text2vec embeddings](https://github.com/shibing624/text2vec).


*Figure 1: Association strength, also known as embedding bias, between gender and target words in different embedding space.*
<sub><sup>*Technically, the cosine similarity between the embedding of each target word and the gender direction extracted from the embedding space is plotted.*</sup></sub>
![image](https://github.com/user-attachments/assets/e3fc8e81-4f4e-437c-98b7-35cbc3c25633)


The first notable observation is that all target words align more closely with the male direction in text2vec, suggesting the existence of gender bias within the text2vec embedding space. The biased embedding is a reflection of the gender stereotypes present in the corpus. On the other hand, the gender bias differs between the two corpora. Firstly, the appearance target words exhibit a bias towards females in both corpora. However, the life target words remain neutral in Corpus 2 while being biased towards females in Corpus 1. Additionally, the acting and writing words in Corpus 2 tend to be gender-neutral, while in Corpus 1 they exhibit a slight bias towards males. 

  <!---
### Word Clusters
 Embeddings capture meaningful semantic information of words; however, interpreting them directly can be challenging. One commonly used technique for interpretation is the projection of word embeddings in lower dimensions as in [Figure 2]<> (https://github.com/user-attachments/assets/05e7f981-e65b-4325-bf62-9a2b6c73a3b1). 

 ![image](https://github.com/user-attachments/assets/05e7f981-e65b-4325-bf62-9a2b6c73a3b1)

 It turns out that the separation between target classes are clearly reflected in the trained embeddings. Based on the first PCA component (x-axis), we observe clear separation between the words in the life target class (associated with the theme <> and feeling of movies) and the other 4 classes, which are related to the technical aspects of movies, such as acting and directing. Moreover, the second component (y-axis) enables a tentative classification between the words in the writing target <> class and those in the acting and directing classes, particularly in Corpus 2.

-->

## Methodology and Data
Details of the methodology and more analysis results can be found in the [report](https://github.com/maggie980000/embedding-bias/blob/main/course_project_embedding_bias.pdf) and the code to reproduce all results in the report can be found in this [notebook](https://github.com/maggie980000/embedding-bias/blob/main/word_embedding_notebook.ipynb).
The original movie review corpora can be downloaded from [here](https://github.com/SophonPlus/ChineseNlpCorpus/blob/master/datasets/dmsc_v2/intro.ipynb).
