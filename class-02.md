# Explore the Tech!

## 1. Unit Testing and TDD in Python:
TDD stands for Test-Driven Development.
Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.
The test file name should follow the same name of module name. For instance, if our module is `gender.py`, our test name should be `test_gender.py`. 
It’s ideal to separate the tests folder from production code (the implementation).

***AAA: Arrange, Act and Assert.***
* Arrange: you need to organize the data needed to execute that piece of code (input);
* Act: here you will execute the code being tested (exercise the behaviour);
* Assert: after executing the code, you will check if the result (output) is the same as you were expecting.

***TDD Cycle:***
* Write a unit test and make it fail.
* Write the feature and make the test pass.
* Refactor the code.

***Interesting Fact:*** 
One of the things that are amazing about TDD is how we can grow our software design consciously and well.
Just building what is needed to make the test pass.
When we are writing tests we are forced to think about the design first and how we can break it into small pieces.


## 2. Recursion:
The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function.
In the recursive program, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems. 
The idea is to represent a problem in terms of one or more smaller problems, and add one or more base conditions that stop the recursion. For example, we compute factorial n if we know factorial of (n-1). The base case for factorial would be n = 0. We return 1 when n = 0. 

**Example:**
```
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}
```


* **Note:** If the base case is not reached or not defined, then the stack overflow problem may arise. 

***Types of Recursion:***
1. Direct and Indirect.
2. Tailed and Non-tailed.
