# Word Vectors - Game of Thrones
Este código foi desenvolvido no vídeo ["How to Make Word Vectors from Game of Thrones (LIVE)"](https://www.youtube.com/watch?v=pY9EwZ02sXU) de Siraj Raval.

A seguir uma lista de alterações que você deve realizar no código para ficar compatível com as atualizações da biblioteca Gensim.

1) Substitua:
print("Word2Vec vocabulary length:", len(thrones2vec.vocab))

por

print("Word2Vec vocabulary length:", len(thrones2vec.wv.vocab))


2) Substitua:
thrones2vec.train(sentences)

por

thrones2vec.train(sentences, total_examples=thrones2vec.corpus_count, epochs=30)


3) Substitua:
all_word_vectors_matrix = thrones2vec.syn0

por

all_word_vectors_matrix = thrones2vec.wv.vectors

##Overview

This is the code for [this](https://www.youtube.com/watch?v=pY9EwZ02sXU) live session on youtube by Siraj Raval. We used 5 books in the [Game of Thrones](https://en.wikipedia.org/wiki/Game_of_Thrones) series to create a set of [word vectors](https://en.wikipedia.org/wiki/Word2vec). We'll use them to the find the similarity between words, map them out in 2D space, and analyze them.


##Dependencies

run `pip install -r pip-requirements.txt` to install the necessary dependencies. 


##Usage

The `demo.ipynb` has my commented code. The `Thrones2vec.ipynb` has the precompiled code, so you can see what the plots look like.


##Credits

Credits for this code go to [Yuriy Guts](https://github.com/YuriyGuts/). I've merely created a wrapper to get people started.



