# Explore the Tech!

## 1. Classes and Objects in Python:

Objects are an encapsulation of variables and functions into a single entity. 
Objects get their variables and functions from classes. Classes are essentially a template to create your objects.

```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")
```
###### Accessing Object Variables:
```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()

myobjectx.variable
```
You can create multiple different objects that are of the same class(have the same variables and functions defined). 

However, each object contains independent copies of the variables defined in the class. 
```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()
myobjecty = MyClass()

myobjecty.variable = "yackity"

# Then print out both values
print(myobjectx.variable)
print(myobjecty.variable)
```


## 2. Recursion in Python:
A recursive function is a function defined in terms of itself via self-referential expressions.

This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result.
All recursive functions share a common structure made up of two parts: base case and recursive case.

###### Example:
```
def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1

    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)
```

When dealing with recursive functions, keep in mind that each recursive call has its own execution context, so to maintain state during recursion you have to either:

Thread the state through each recursive call so that the current state is part of the current call’s execution context.

###### Recursive Data Structures in Python
A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. A list is an example of a recursive data structure. 

## 3. Pytest in Python:
###### Fixtures:
In some cases in testing, things are a bit complex. You'll want to have some objects available to all of your tests. Those objects might contain data you want to share across tests, or they might involve the network or filesystem. These are often known as "fixtures" in the testing world, and they take a variety of different forms.

In pytest, you define fixtures using a combination of the `pytest.fixture` decorator, along with a function definition.

* Example: 
```
@pytest.fixture
def simple_file():
   return StringIO('\n'.join(['abc', 'def', 'ghi', 'jkl']))
```

###### Coverage:
checks that your tests have run all of the code.
So, how can you include code coverage with pytest? 
It turns out that there's a package called `pytest-cov` on PyPI that you can download and install. 
Once that's done, you can invoke pytest with the `--cov` option.
If you don't say anything more than that, you'll get a coverage report for every part of the Python library that your program used,
so I strongly suggest you provide an argument to `--cov`, specifying which program(s) you want to test.
And, you should indicate the directory into which the report should be written. So in this case, you would say:
`pytest --cov=mymul`
`coverage html`: activate.
