# Read:09 Summary
## Dunder Methods

### What Are Dunder Methods?

* In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end
with double underscores, for example `__init__ or __str__.`
* As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”
* These “dunders” or “special methods” in Python are also sometimes called “magic methods.
* Dunder methods let you emulate the behavior of built-in types
* Object Initialization: `__init__` : 
  * Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor
  which in Python is the` __init__ dunder`
* `__repr__` :  The “official” string representation of an object. This is how you would make an object of the class. The goal 
of` __repr__ `is to be unambiguous.

* `__str__`: The “informal” or nicely printable string representation of an object. This is for the enduser.
* `Callable Python Objects: __call__ `: You can make an object callable like a regular function by adding the` __call__ dunder` method
-------------------------------------------------------------------------------------------------------------------------------
## Basic Statistics in Python — Probability

* At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?”
* The normal distribution refers to a particularly important phenomenon in the realm of probability and statistics. 

* The normal distribution is significant to probability and statistics thanks to two factors: the Central Limit Theorem and the Three Sigma Rule.
* `Z-score` :  The Z-score is a simple calculation that answers the question, “Given a data point, how many standard deviations is it away from the mean?”
* Statistics doesn’t have to be a field relegated to just statisticians. As a data scientist, having an intuitive understanding on common statistical measures
represent will give you an edge on developing your own theories and the ability to subsequently test these theories
