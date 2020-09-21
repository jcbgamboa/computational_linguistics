---
layout: page
---


W4 Corpus Linguistics (part 2)
==============================

Continuing our Python/NLTK tutorial
-----------------------------------

Our goal this week is to learn how to compare different datasets. However,
for that, we will go through a lot of "preparation steps", learning how to
open files, revisiting how list comprehensions work, etc.
This week videos are a little more practical. Hopefully this is useful.

<iframe width="560" height="315" src="https://www.youtube.com/embed/VP1YdXqjaqM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/pELYqAhv_5g" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/hegHv-lhhDw" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/LH4-zakDWX4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


Language Modeling
-----------------

In the weekly synchronous meetings, I mentioned that this week would cover
some Language Modeling. However, since I
feel that I'd be doing redundant work if I created videos on this topic (but
also because I want to save time) I decided to not make any videos. I will
present a "curated" list of materials here, which I hope are going to be
useful.

* First, I think you should watch the videos 1 to 5 of the part on Language
  Models of the Stanford course on NLP:
    * [https://www.youtube.com/watch?v=Saq1QagC8KY&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=12](https://www.youtube.com/watch?v=Saq1QagC8KY&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=12)
        * There is a chance you are not used to the rule
          $P(a,b) = P(b|a)P(a)$, that he talks about. This is the
          "Bayes's Rule" or "Bayes's Theorem". If you want to understand
          it better, the 3Blue1Brown has an awesome video explaining it:
            * [https://www.youtube.com/watch?v=HZGCoVF3YvM](https://www.youtube.com/watch?v=HZGCoVF3YvM)
        * You might also want to know better about the Markov Assumption.
          The Khan Academy has a good and intuitive video on the topic:
            * [https://www.youtube.com/watch?v=Ws63I3F7Moc](https://www.youtube.com/watch?v=Ws63I3F7Moc)
    * [https://www.youtube.com/watch?v=paCMAZ-lKq8&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=13](https://www.youtube.com/watch?v=paCMAZ-lKq8&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=13)
        * You might find this video a little complicated. Honestly, I only
          added it here because it is referred back in future videos. I
          actually preferred (and recommend) the explanation of another video,
          which I think you might want to watch if you don't understand well
          how the formulas work together here. It also has good examples of
          applications:
            * [https://www.youtube.com/watch?v=GiyMGBuu45w](https://www.youtube.com/watch?v=GiyMGBuu45w)
    * [https://www.youtube.com/watch?v=b6nwdc_fGfA&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=14](https://www.youtube.com/watch?v=b6nwdc_fGfA&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=14)
        * Do not worry much if you do not understand how exactly Perplexity
          works. The important part for this video is to understand the
          separation of the entire dataset into "Training set" and "Test set".
          We will come back to this separation when we talk about Machine
          Learning in a future class.
    * [https://www.youtube.com/watch?v=6NeUDr7YDiw&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=15](https://www.youtube.com/watch?v=6NeUDr7YDiw&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=15)
        * At this point, I think it would probably be interesting for you read
          sections 2, 3 and 4 (in pages 4 to 8) of the paper
          ["A mathematical theory of communication"](http://people.math.harvard.edu/~ctm/home/text/others/shannon/entropy/entropy.pdf)
          (Shannon, 1948).
          The "Shannon visualization method" that is referred to in the video
          comes from this part of the paper.
    * [https://www.youtube.com/watch?v=ZbHFLgBWgdQ&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=16](https://www.youtube.com/watch?v=ZbHFLgBWgdQ&list=PLQiyVNMpDLKnZYBTUOlSI9mi9wAErFtFm&index=16)

* Ok... but what do people actually use for Language Modeling? For a few of
  years, certain Recurrent Neural Networks became really popular. Nowadays, the
  most popular model is the GPT-2 model. On this, I'd like you to watch/read the
  following:
    * The Computerphile has a very easy-to-understand video that speaks a little
      about RNNs: [https://www.youtube.com/watch?v=rURRYI66E54](https://www.youtube.com/watch?v=rURRYI66E54)
        * (OFF TOPIC) This video is actually followed by a series of other
          videos, which I'll put here just in case you are interested:
            * [https://www.youtube.com/watch?v=89A4jGvaaKk](https://www.youtube.com/watch?v=89A4jGvaaKk)
            * [https://www.youtube.com/watch?v=p-6F4rhRYLQ](https://www.youtube.com/watch?v=p-6F4rhRYLQ)
            * [https://www.youtube.com/watch?v=AJxLtdur5fc](https://www.youtube.com/watch?v=AJxLtdur5fc)
    * I would like you to read Andrej Karpathy's
      [The Unreasonable Effectiveness of RNNs](https://karpathy.github.io/2015/05/21/rnn-effectiveness/)
        * Do not worry much if there are things that are unclear/confusing. Pay
          attention mostly to the applications of RNNs. We will come back to
          this text again in a future week, and at that point you'll hopefully
          be able to understand more.

This looks like a lot of materials, but you'll notice that you can go through
the videos in 1h~2h. Then you'll only need to read the two text materials,
which may take some 2h more.

From all of this, there are a few concepts that I think are crucial to
understand and some others that are just interesting.I thought I'd try to
"guide" you to pay attention to certain topics more than others. Here is a list
of what I think is important that you understand from the materials:

* What are n-grams
* What are Language Models
* What are Language Models useful for? What are some of the applications?
* How to calculate the probability of a sentence from a bi-gram model?
* The division between "Training set" and "Test set" (we will revisit this topic again in the future)
* What is smoothing?
* Why do you want smoothing?
* What is Laplace smoothing? (It is called "Add one smoothing" in the videos)
* How language models generate sentences? (That is, the "word-by-word" process)
* That RNNs are good for processing sequences

Additional Materials
--------------------

I found this playlist in Youtube which goes well along with the Corpus
Linguistics topic. This might be a nice place for you to start if you are
interest in the topic.

[https://www.youtube.com/watch?v=SZ2RtyKzU6o&list=PLKgdsSsfw-fau4PsTEOCcXsKxSmk6pJTY&index=1](https://www.youtube.com/watch?v=SZ2RtyKzU6o&list=PLKgdsSsfw-fau4PsTEOCcXsKxSmk6pJTY&index=1)
 
