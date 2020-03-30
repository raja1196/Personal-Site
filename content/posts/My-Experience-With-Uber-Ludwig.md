+++
title = "My Experience With Uber Ludwig"
date = 2020-03-29T15:42:50-04:00
draft = true
description = "Sharing my experience using Uber Ludwig"
type = ["posts","post"]
tags = [
    "Python",
    "Uber",
    "Ludwig",
    "Tutorial",
    "AutoML",
]
series = ["Testing Opensource AutoML tools"]
[ author ]
  name = "Rajaram Sivaramakrishnan"
+++
## Introduction

Imagine not having to type lines and lines of code, looking at the screen for hours not knowing why the script won't run. This is one of the prime reasoning behind the development of Uber's AutoML AI platform, Ludwig.

So, how do they manage to do this? Is the toolbox easy to use? Do you need a lot of GPU resources to run it? To answer all these questions, I am going to test the toolbox by running an experiment from start to finish. Along the way, I will also show how to setup your environment to run ludwig effectively.


### Pre Requisites:

There are two ways to install ludwig in your system, and the good thing is that it is a single line command, that is OS agnostic. But in order to make use of that, we must have python installed in the system. There are two ways to do that. 

I am adding links on how to do for either case. 
1. [Directly](https://realpython.com/installing-python/) install python and create a [virtual environment](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/).
2. Use [Miniconda](https://resbaz.github.io/resbook-installation/python.html#installing-python-with-miniconda), an offering from Anaconda inc. to have python and conda create a [virtual environment](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/).

Now that is done, Et voilà! (there you go!).

```python
 $ pip install ludwig
```
To install task specific packages, add [] after ludwig to enter one of more from the following categories. 

Text, Viz, image, audio, serve 

As an example, I will be using image dataset, so we can specifically install,

```python
 $ pip install ludwig[image]
```

Or if you will need cross-platform support, dealing with multiple data types, you can install the full package by using the command,

```python
 $ pip install ludwig[full]
```

To be clear, all of this are well documented in [Ludwig's](https://uber.github.io/ludwig/getting_started/) website. But this is my experience following that and as user of the toolbox, see how simple it is. 

### Experiment:
In this blog, I will use ludwig's toolbox to classify emotions with facial emotion recognition. The [dataset](https://github.com/microsoft/FERPlus) can be downloaded from the Github repository. The toolbox necessitates use of CSV file as the dataset, and I could'nt figure a way around it yet. 

