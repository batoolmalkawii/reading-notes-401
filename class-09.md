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
