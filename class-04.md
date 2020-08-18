# Read:04 Summary
## Classes and Objects
* `Objects` :  are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes.
* `Classes ` : are essentially a template to create your objects.
* ` class MyClass:`
   ` variable = "blah"`

    `def function(self):`
       ` print("This is a message inside the class.")`

`myobjectx = MyClass() `
### Accessing Object Variables
* we can di it using `myobjectx.variable`
### Accessing Object Functions

* we can do it using `myobjectx.function()`
-----------------------------------------------------------------------------------------------------------------------------
## Thinking Recursively in Python

* typical structure of a recursive algorithm. If the current problem represents a simple case, solve it. If not, divide it into 
subproblems and apply the same strategy to them
*  `A recursive function`: is a function defined in terms of itself via self-referential expressions.
  * This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result
  
***When dealing with recursive functions, keep in mind that each recursive call has its own execution context***

* Recursive Data Structures in Python
  * A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. A list is
  an example of a recursive data structure
  
-------------------------------------------------------------------------------------------------------------------------------------
## Python Testing with pytest

* there are two features of pytest :
  * Fixtures
  * code coverage

### fixtures 
* You'll want to have some objects available to all of your tests. Those objects might contain data you want to share
across tests, or they might involve the network or filesystem. These are often known as "fixtures" in the testing world, and they take
a variety of different forms.
* define fixtures using a combination of the pytest.fixture decorator, along with a function definition.
### coverage
* when software gets larger and more complex, it's not going to be so easy to eyeball it. That where you want to have "code coverage", checking that
your tests have run all of the code.

* Now, 100% code coverage doesn't mean that your code is perfect or that it lacks bugs. But it does give you a greater degree of
confidence in the code and the fact that it has been run at least once.
* you can invoke pytest with the `--cov` option you'll get a coverage report for every part of the Python library that your program used

-----------------------------------------------------------------------------------------------------------





