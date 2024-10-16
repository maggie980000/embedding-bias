
# Gender Bias in Word Embeddings Trained on Movie Review Corpora


Embeddings are numerical representations of words. Embeddings of words with similar semantic meanings are associated closely to each other, since they are likely to appear together in natural language.

## Findings and Graphics


### Gender Bias 


In [Figure 1](https://github.com/user-attachments/assets/fd63aaab-d7c4-4434-8dcd-6c146f25b54f), I investigate the association strength, also known as embedding bias, between gender and 5 manually selected classes of target words in 3 distinct word embedding space:
- Word embeddings trained from the Corpus 1, i.e. reviews on the movies “Tiny Times 1.0” (2013) or “Tiny Times 3.0” (2014).
- Word embeddings trained from the Corpus 2, i.e. reviews on the movie “La La Land” (2016).
- Pre-trained [text2vec embeddings](https://github.com/shibing624/text2vec).

![image](https://github.com/user-attachments/assets/fd63aaab-d7c4-4434-8dcd-6c146f25b54f)

The first notable observation is that all target words align more closely with the male direction in text2vec, suggesting the existence of gender bias within the text2vec embedding space. The biased embedding is a reflection of the gender stereotypes present in the training corpus. On the other hand, the gender bias differs between the two corpora. Firstly, the appearance target words exhibit a bias towards females in both corpora. However, the life target words remain neutral in Corpus 2 while being biased towards females in Corpus 1. Additionally, the acting and writing words in Corpus 2 tend to be gender-neutral, while in Corpus 1 they exhibit a slight bias towards males. 
  
### Word Clusters
Embeddings capture meaningful semantic information of words; however, interpreting them directly can be challenging. One commonly used technique for interpretation is the projection of word embeddings in lower dimensions as in [Figure 2](https://github.com/user-attachments/assets/05e7f981-e65b-4325-bf62-9a2b6c73a3b1). 

![image](https://github.com/user-attachments/assets/05e7f981-e65b-4325-bf62-9a2b6c73a3b1)

It turns out that the difference between target classes are reflected in the trained embeddings. Based on the first PCA component (x-axis), we observe clear separation between the words in the life target class (associated with the theme and feeling of movies) and the other 4 classes, which are related to the technical aspects of movies, such as acting and directing. Moreover, the second component (y-axis) enables a tentative classification between the words in the writing target class and those in the acting and directing classes, particularly in Corpus 2.

## Methodology and Data
Details of the methodology can be found in the [report](https://github.com/maggie980000/embedding-bias/blob/main/course_project_embedding_bias.pdf). 
The 2 movie review corpora can be downloaded [here](https://github.com/SophonPlus/ChineseNlpCorpus/blob/master/datasets/dmsc_v2/intro.ipynb).
