# Read:06 Summary
## How to use the Random Module in Python

* `The random module` : provides access to functions that support many operations.the most important thing is that it allows you to generate random numbers.
## When to use it?

* when We want the computer to pick a random number in a given range 

### Random functions 
* `Randint` : If we wanted a random integer, we can use it and it accepts two parameters
* Ex : 
* `import random`
* `print random.randint(0, 5)`
--------------------------------------
* `Random` : 
* If you want a larger number, you can multiply it.
* Ex :
* `import random`
* `random.random() * 100`
--------------------------------------
* `Choice` : Generate a random value from the sequence , or random value from a list 
* Ex
* `import random`
* `myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]`
* `random.choice(myList)`
---------------------------------------
* Shuffle : shuffles the elements in list in place, so they are in a random order.
* Ex
* `from random import shuffle`
* `x = [[i] for i in range(10)]`
* `shuffle(x)`
-------------------------------------
* `Randrange` : Generate a randomly selected element from range(start, stop, step)
* Ex
* `import random`
* `for i in range(3):`
* `    print random.randrange(0, 101, 5)`
----------------------------------------------------------------------------------------------------------------------------------------
## What is Risk Analysis in Software Testing ?
* `risk analysis` : is the process of identifying the risks in applications or software that you built and prioritizing them to test
### Why use Risk Analysis?
* it highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks. When a test
plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause 
to your software along with solutions.


***possible risks that you could encounter :***


  * Use of new hardware

  * Use of new technology

  * Use of new automation tool

  * The sequence of code

  * Availability of test resources for the application

***unavoidable risks***
  * The time that you allocated for testing


  * A defect leakage due to the complexity or size of the application


  * Urgency from the clients to deliver the project


  * Incomplete requirements
  
### Risk Identification
* Risk Identification : come from your company or your customer,
* Testing Risks : come from the platform you are working on
* Premature Release Risk : come from releasing unsatisfactory or untested software
* Software Risks : come from the software development process.

### Risk Assessment
* There are three perspectives of Risk Assessment:
  * Effect
  * Cause
  * Likelihood

### How to perform Risk Analysis?
* There are three steps:
  * Searching the risk


  * Analyzing the impact of each individual risk


  * Measures for the risk identified


------------------------------------------------------------------------------------------------------------------------------------------------
## Dependency Injection: what it is ???
* Dependency or dependent means relying on something for support
* `Dependency Injection`: is a technique whereby one object (or static method) supplies the dependencies of another object. A dependency is an object that
can be used (a service).

***`Dependency Injection` : transferring the task of creating the object to someone else and directly using the dependency***

### three types of dependency injection:

  * `constructor injection`: the dependencies are provided through a class constructor.
  
  * `setter injection` : the client exposes a setter method that the injector uses to inject the dependency.

  * `interface injection` : the dependency provides an injector method that will inject the dependency into any client passed to it. Clients must 
  implement an interface that exposes a setter method that accepts the dependency.

### dependency injection’s responsibility to:
  * Create the objects

  * Know which classes require those objects
  
  * And provide them all those objects



































  











