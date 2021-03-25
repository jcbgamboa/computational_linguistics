---
layout: page
---


W6 Machine Learning (part 1)
============================

Notice that the slides for the parts in which I present things are available
(as always) in the Downloads Folder.

Introduction
------------

<iframe width="560" height="315" src="https://www.youtube.com/embed/RV7TW50o7vY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


An introduction to Numpy, Scipy and Matplotlib
----------------------------------------------

<iframe width="560" height="315" src="https://www.youtube.com/embed/kD2Fn1FUeTk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


Classification
--------------

<iframe width="560" height="315" src="https://www.youtube.com/embed/hlcdWdNI_6s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



Generating toy data
-------------------

(after watching video 3)

Before watching the next video, I'd like to introduce a piece of code that I'll
assume you already understand when talking about it in the video.

In the previous video, I generated data using

```python
1 data = np.random.random_sample([1000, 2])
2 labels = data[:,0] + data[:,1] > 1
```
and plotted it using

```python
3 plt.plot(data[:,0], data[:,1], 'o')
```

### Generating data

I would like to put these the first code snippets into a function called
`make_data_noiseless()`:

```python
1  def make_data_noiseless(num_samples=1000,
2                          label_fct = lambda X: ((X[:,0] +X [:,1]) > 1)):
3    data = np.random.random_sample((num_samples,2))
4
5    # generate labels for all samples
6    labels = label_fct(data)
7
8    return data,labels
```

_(Take care not to interpret the name of the function incorrectly. This is a
function that "makes data", i.e., generates a dataset. Its name contains the
word "noiseless" because all data points are perfectly classified according
to the label function passed as parameter)_

The function receives the number of samples it should generate (the number
of "bank customers", in our previous video) and how the labels should be
assigned. It is likely useful to copy these lines into a jupyter notebook and
play around with them, so that you understand what is going on.

There is a chance you don't understand what that "lambda" is doing there. I
haven't introduced lambda functions in Python to you. If you don't understand
it, I'd like you to either watch the following video:

[https://www.youtube.com/watch?v=25ovCm9jKfA](https://www.youtube.com/watch?v=25ovCm9jKfA)

... or read the beginning of the following text (no need to read the entire
thing, though -- read until you feel you understand how the lambda function
above works):

[https://realpython.com/python-lambda/](https://realpython.com/python-lambda/)

### Plotting data

The second code snippet would go to another function called  `plot_data()`.

```python
1  def plot_data(data, labels):
2     # divides the data into two datasets
3     d0 = data[labels==False]
4     d1 = data[labels]
5
6     # plots the two parts
7     plt.figure(figsize=(6,6))
8     plt.plot(d0[:,0],d0[:,1],"bo")
9     plt.plot(d1[:,0],d1[:,1],"ro")
10
11    # prints in the console how many samples of each type are there
12    print("numbers of samples: %d, %d"%(len(d0),len(d1)))
```

I assume this code is going to be easier to follow, since it is almost identical
to the code in the previous video.


<iframe width="560" height="315" src="https://www.youtube.com/embed/clBrQGRNxSs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>




Preprocessing
-------------

Now you should go to the `Downloads Folder/Week 6/` and read file
`W6 Preprocessing.ipynb`.

The next video will assume that you have read the file and understand most of
its content. If you have troubles with the Bag of Words representations, do not
worry much: the next video will try to clarify it.

<iframe width="560" height="315" src="https://www.youtube.com/embed/-9CmwiD4ou8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



Classification with kNN
-----------------


<iframe width="560" height="315" src="https://www.youtube.com/embed/JSrG8VB3Mj0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



Distance Measures
-----------------

When speaking about the kNN algorithm, I purposefully avoided specifying
explicitly how the distance(d, di) was calculated. This is because there are
several distance measures. Here we will explore two of them: the Euclidean
Distance, and the Manhattan Distance.

 
The
[Euclidean distance](https://en.wikipedia.org/wiki/Euclidean_distance) is the
distance measure you learn from school. It is the shortest path between two
points. So, given a point $a=(x1, y1)$ and another point $b=(x2,y2)$, the
Euclidean Distance is calculated as:

```python
# I'm writing in Python so that you can see how this is calculated
sum_of_squares = ( (x1 - x2)**2 + (y1 - y2)**2 )
euclid_distance = sum_of_squares**(1/2)
```

Notice that the `**2` means "squared", and the `**(1/2)` means "square root of".


The
[Manhattan distance](https://en.wikipedia.org/wiki/Taxicab_geometry), on
the other hand, is a reference to how New York is organized. Since the city
is organized in a grid, it is impossible to move "through the buildings" in
the shortest path to get from place a to place b. Therefore, the distance from
point a to point b is the sum of the "horizontal displacement" (how much you
have to move from left to right / right to left) and the "vertical displacement"
(how much you have to move from the top to bottom / bottom to top).

```python
# "abs" gets the "absolute value", i.e., removes the sign
manhattan_distance = abs(x1 - x2) + abs(y1 - y2)
```
 

This video should be helpful in understanding these distances:
[https://www.youtube.com/watch?v=p3HbBlcXDTE](https://www.youtube.com/watch?v=p3HbBlcXDTE)


Evaluating the performance of our Classifier
--------------------------------------------

<iframe width="560" height="315" src="https://www.youtube.com/embed/6uDYAdgmR8s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



