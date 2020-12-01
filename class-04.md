# Explore the Tech!

1. Classes and Objects in Python:
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
