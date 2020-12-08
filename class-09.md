# Explore the Tech!

## 1. Dunder methods in _Python_:

##### What are dender methods?
In Python, special methods are a set of predefined methods you can use to enrich your classes. 
They are easy to recognize because they start and end with double underscores, for example `__init__` or `__str__`.

As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term _“dunder methods”_, a short form of _“double under.”_

These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing “magical” about them.
You should treat these methods like a normal language feature.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). 
But an empty class definition doesn’t support this behavior out of the box.


##### Enriching Classes
denders unlock the following language features:
* Initialization of new objects. `__init__`
* Object representation. `__str__`, `__repr__`
* Enable iteration. `__len__`, `__getitem__`, `__reversed__`
* Operator overloading (comparison). `__eq__`, `__lt__`
* Operator overloading (addition) `__add__`
* Method invocation. `__call__`
* Context manager support (with statement). `__enter__`, `__exit__`



## 2. Probability in _Python_:

##### What is probability?
At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest.
To calculate the chance of an event happening, we also need to consider all the other events that can occur. 
The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:
* Flipping a heads.
* Flipping a tails.

##### The data and the distribution
Intuitively, we’d like to use the scores of the wines to compare groups, but there comes a problem: the scores usually fall in a range. 
How do we compare groups of scores between types of wines and know with some degree of certainty that one is better than the other? 
Enter the **normal distribution**. The normal distribution refers to a particularly important phenomenon in the realm of probability and statistics.

In a probability context, the high point in a normal distribution represents the event with the highest probability of occurring. 
As you get farther away from this event on either side, the probability drops rapidly, forming that familiar bell-shape. 
The high point in a statistical context actually represents the mean. As in probability, as you get farther from the mean, you rapidly drop off in frequency. 
That is to say, extremely `high` and `low` deviations from the `mean` are present but exceedingly rare.

If we visualize each group of scores as normal distributions, we can immediately tell if two distributions are different based on where they are.
We assume the scores will be normally distributed since we have a ton of data.

