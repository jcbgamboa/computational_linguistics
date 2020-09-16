W9 Distributional Semantics (part 1)
====================================

So... this week we will learn about a way to represent words using vectors.
Each word vector is contructed based on the kinds of contexts in which the
words appear, and this follows from the Distributional Hypothesis, that states
that a word's meaning is dependent on the contexts in which the words appear.

Now, the procedure we will follow is not the only procedure possible. You'll
find more information on current procedures in the "Additional Materials" below.
For this course, I'll expect that you know how to calculate co-occurrences and
how to build a co-occurrence matrix.

Notice how our vectors (and actually many vectors you'll find on the internet)
don't care about our entire discussion on "Polysemy" and "Homonymy". For them,
the word "bank" is a single word with many meanings, and hopefully the vector
associated with "bank" will capture both the information related to "river bank"
and the information related to "financial institution". We will come back to
this topic in the next week.


A note on Terminology
---------------------

The "word vectors" that are the main topic of this week are also very often
referred to as "word embeddings". Beware that the videos I refer to use these
names. "Word vectors" and "word embeddings" or even "vector embeddings" are
just the same.


Applications
------------

After preparing these materials, I felt that you may find it pointless to
transform the words into vectors. What do these vectors "mean"? What can we do
with them? We don't really get to say what is the actual "meaning" of a word.
At most, from these vectors, we are able to say "which words are similar"...
but that is all.

Still... these embeddings are frequently used as input to Machine Learning
models. In a way, transforming the sentences into embeddings is often seen as
part of the "preprocessing stage" of many Machine Learning applications. You
can see a current example for Machine Translation (in which they use the
"Glove vectors" -- pretrained vectors that you can download from the internet)
in the following video:

[https://www.youtube.com/watch?v=TQQlZhbC5ps](https://www.youtube.com/watch?v=TQQlZhbC5ps)

Additional Materials
--------------------

The way in which we produced our word vectors in this class is just one way to
do it. This is a quite "unsophisticated" way of doing it nowadays. I didn't
want to go further into the newer methods because they would require a lot more
math. Still... I think that you should know that they exist.

Up to ~2018 the most popular way of creating word vectors that quite faithfully
represented the meanings of the words was "word2vec". The videos in the
following two links explain the idea (they talk about the same thing). They may
be quite hard to understand. I am putting them here only so that you know what
to look for in case you are interested in more information.

[https://www.youtube.com/watch?v=ERibwqs9p38](https://www.youtube.com/watch?v=ERibwqs9p38)
[https://www.youtube.com/watch?v=QyrUentbkvw](https://www.youtube.com/watch?v=QyrUentbkvw)

The newest way to create word vectors is BERT. This is the current
"state-of-the-art" model. It is based on a Neural Network architecture commonly
referred to as "transformer". In a way, it may be that the BERT vectors do take
into account the no-homonymy problems of their predecessors (but I am not really
100% clear on how BERT works, so I can't really say). You can get more
information on BERT in the following video:

[https://www.youtube.com/watch?v=xI0HHN5XKDo](https://www.youtube.com/watch?v=xI0HHN5XKDo)


Co-occurrences
--------------

(after watching video 1)

Before watching the next video, please read the file
"W9 Context and Co-occurrences.ipynb" from the Download Folder.

It will describe how we convert our words into vectors, which we will then
compare to be able to tell whether words are semantically similar.


