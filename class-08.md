# Explore the Tech!

## List Coprehensions:


List comprehensions provide a concise way to create _lists_.
It consists of brackets containing an expression followed by a for clause, then
zero or more for or if clauses. The expressions can be anything, meaning you can
put in all kinds of objects in lists.

The result will be a new list resulting from evaluating the expression in the
context of the for and if clauses which follow it.

The list comprehension always returns a result list.

The list comprehension starts with a `‘[‘ and ‘]’`, square brackets, to help you remember that the
result is going to be a list.

The basic syntax uses square brackets.
```
[ expression for item in list if conditional ]
```

This is equivalent to:
```
for item in list:
    if conditional:
        expression
```



