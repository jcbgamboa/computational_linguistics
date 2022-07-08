---
layout: page
---


W11 Wrapping Up
===============



I prepared a "W11\_VectorEmbeddings.ipynb" file containing the content of this week.
The first two "parts" are presented in the videos.
(but do note that there is more content that is only accessible in the Jupyter Notebook)

This week I had planned to speak a little about Language Models.
I felt, however, that everything that I had to say was already said, and
whatever was "left" was only going to be a lot of math, that I didn't feel would
be useful for you. So I changed my mind and created this content with some more
exploration of "Distributional Semantics". The goals are the following:

 * To explore a little more these word vectors (that everyone keeps using and
   talking about these days)
 * To show you one way that you can just "access" the word vectors, without
   having to train a Machine Learning model, or deal with too many complications.
   In our case, we will use a Python library called Flair.
 * To show you some of the "limitations" of these vectors, and try to help you
   get some intuition of what they are doing.

Because this class is so "unorthodox", almost none of this will appear in the
exam. There are only two things that I want you to know from this class (that
may appear in the exam):

 * Why BERT vectors are called "contextual" word vectors.
 * Word vectors do not represent synonymy (at least not in the way we are used
   to thing about it)

"Exercise"
----------

I know I said there would be exercises for this class. Unfortunately, I was not
able to come up with ideas for questions. My plan for this class is to go
through the notebook along with you.

(Also... do note that the notebook is slightly different from the video, because
I made changes to it after I recorded the videos.)

Additional Materials
--------------------

 * In one of the videos, I mentioned GANs (Generative Adversarial Networks).
   As far as I know, these networks were the first networks to show the properties
   we explored in the first video (i.e., that it was possible to do some sort of
   "arithmetic" with the representations learnt by the networks).
   [The Computerphile has a video on these that may be interesting](https://www.youtube.com/watch?v=Sw9r8CL98N0)
 * Indeed, the Computerphile also has
   [a video on the vector embeddings](https://www.youtube.com/watch?v=gQddtTdmG_8),
   where they
   mention the embedding arithmetic that I was trying to do (and they show that
   it worked with Word2Vec algorithm), but they do it in a somewhat different way.

Where to go from here?
----------------------

That is all for this course. I hope the course was useful. Thank you for your
participation. In the next week there will only be a Q&A + Feedback, and then
in the other week we have the exam.

The techniques we explored this week are quite new, and still relatively “hot”
in the NLP literature. If you are interested in them, then you should probably
take a look at the
[Stanford course on Natural Language Processing with Deep Learning](https://www.youtube.com/playlist?list=PLoROMvodv4rOhcuXMZkNm7j3fVwBBY42z),
which will talk about them in more details.


