# Explore the Tech!

## 1. Random Module in Python:

The Random module contains some very useful functions.

##### Randint
If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number.
Generate integers between 1,5. The first value should be less than the second.
  ```
  import random
  print random.randint(0, 5)
  ```
  
##### Random
If you want a larger number, you can multiply it.

For example, a random number between 0 and 100:
```
import random
random.random() * 100
```


##### Choice
Generate a random value from the sequence sequence.
```
random.choice( ['red', 'black', 'green'] ).
```
The choice function can often be used for choosing a random element from a list.
```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```

##### Shuffle
The shuffle function, shuffles the elements in list in place, so they are in a random order.
```
random.shuffle(list) Example taken from this post on Stackoverflow
```
```
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
```

##### Randrange
Generate a randomly selected element from range(start, stop, step)
```
random.randrange(start, stop[, step])
import random
for i in range(3):
    print random.randrange(0, 101, 5)
```


## 2. Risk Analysis in Software Testing

In Software Testing, risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. 
After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.

##### Why use Risk Analysis?
* In any software, using risk analysis at the beginning of a project highlights the potential problem areas. 
* After knowing about the risk areas, it helps the developers and managers to mitigate the risks. 
* When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.

##### Risk Identification
There are different sets of risks included in the risk identification process. Those are as follows:

1. **Business Risks**: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

2. **Testing Risks**: You should be well acquainted with the platform you are working on, along with the software testing tools being used.

3. **Premature Release Risk**: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

4. **Software Risks**: You should be well versed with the risks associated with the software development process.

##### Risk Assessment
There are three perspectives of Risk Assessment:

* **Effect** – To assess risk by Effect. In case you identify a condition, event or action and try to determine its impact.

* **Cause** – To assess risk by Cause is opposite of by Effect. Initialize scanning the problem and reach to the point that could be the most probable reason behind that.

* **Likelihood** – To assess risk by Likelihood is to say that there is a probability that a requirement won’t be satisfied.

##### How to perform Risk Analysis?

1. Searching the risk.
2. Analyzing the impact of each individual risk.
3. Measures for the risk identified.
