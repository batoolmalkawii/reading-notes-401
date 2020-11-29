# Explore the Tech!

## 2. Unit Testing and TDD in Python:
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


2. 
