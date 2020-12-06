# Explore the Tech!

## Scopes in Python:
The concept of scope rules how variables and names are looked up in your code. 
It determines the visibility of a variable within the code. The scope of a name or variable depends on the place in your code where you create that variable. 
The Python scope concept is generally presented using a rule known as the **LEGB** rule.

The letters in the acronym LEGB stand for _Local, Enclosing, Global, and Built-in scopes_. This summarizes not only the Python scope levels but also the sequence of steps that Python follows when resolving names in a program.

The scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, functions, objects, and so on. 
A name will only be visible to and accessible by the code in its scope. Several programming languages take advantage of scope for avoiding name collisions and unpredictable behaviors. 
Most commonly, you’ll distinguish two general scopes:

  1. **Global scope:** The names that you define in this scope are available to all your code.

  2. **Local scope:** The names that you define in this scope are only available or visible to the code within the scope.
  
  Since _Python_ is a dynamically-typed language, variables in Python come into existence when you first assign them a value. On the other hand, functions and classes are available after you define them using def or class, respectively.
  Finally, modules exist after you import them.
  
  In Python, the concept of **scope** is closely related to the concept of the **namespace**. A Python scope determines where in your program a name is visible.
  Python scopes are implemented as dictionaries that map names to objects. These dictionaries are commonly called namespaces. 
  These are the concrete mechanisms that Python uses to store names. They’re stored in a special attribute called `.__dict__.`.
  
  ##### Using the LEGB Rule for Python Scope
Python resolves names using the so-called _LEGB_ rule, which is named after the Python scope for names.
The letters in LEGB stand for Local, Enclosing, Global, and Built-in. Here’s a quick overview of what these terms mean:

* **Local** (or function) scope is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. 
These names will only be visible from the code of the function. 
It’s created at function call, not at function definition, so you’ll have as many different local scopes as function calls. 
This is true even if you call the same function multiple times, or recursively. Each call will result in a new local scope being created.

* **Enclosing** (or nonlocal) scope is a special scope that only exists for nested functions.
If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. 
This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

* **Global** (or module) scope is the top-most scope in a Python program, script, or module.
This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.

* **Built-in** scope is a special Python scope that’s created or loaded whenever you run a script or open an interactive session.
This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. 
Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.
