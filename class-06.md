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
