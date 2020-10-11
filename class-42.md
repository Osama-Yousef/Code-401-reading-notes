# Read:42 Summary
## Dunder Methods
* In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with
double underscores, for example __init__ or __str__.
* As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

* These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than
they really are—at the end of the day there’s nothing “magical” about them. You should treat these methods like a normal language feature.
* Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class
definition doesn’t support this behavior out of the box
* This elegant design is known as the Python data model and lets developers tap into rich language features like sequences, iteration, operator overloading, 
attribute access, etc.
* You can see Python’s data model as a powerful API you can interface with by implementing one or more dunder methods. If you want to write more Pythonic code,
knowing how and when to use dunder methods is an important step.
### Object Initialization: __init__
*  constructor which in Python is the __init__ dunder
* The constructor takes care of setting up the object. In this case it receives the owner name, an optional start amount and defines an internal 
transactions list to keep track of deposits and withdrawals.

### Object Representation: __str__, __repr__
* It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are
two ways to do this using dunder methods:
  * __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.


  * __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

### Iteration: __len__, __getitem__, __reversed__
* In order to iterate over our account object I need to add some transactions. So first, I’ll define a simple method to add transactions.
### Operator Overloading for Comparing Accounts: __eq__, __lt__
* We all write dozens of statements daily to compare Python objects.
* This feels completely natural, but it’s actually quite amazing what happens behind the scenes here. Why does > work equally well on integers,
strings and other objects (as long as they are the same type)? This polymorphic behavior is possible because these objects implement one or more 
comparison dunder methods.
### Operator Overloading for Merging Accounts: __add__
* In Python, everything is an object. We are completely fine adding two integers or two strings with the + (plus) operator, it behaves in expected ways
### Callable Python Objects: __call__
* You can make an object callable like a regular function by adding the __call__ dunder method. For our account class we could print a nice report of all the 
transactions that make up its balance
### Context Manager Support and the With Statement: __enter__, __exit__

* A context manager is a simple “protocol” (or interface) that your object needs to follow so it can be used with the with statement. Basically all 
you need to do is add __enter__ and __exit__ methods to an object if you want it to function as a context manager.
------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Iterators
* Iterators provide a sequence interface to Python objects that’s memory efficient and considered Pythonic. Behold the beauty of the for-in loop!
* To support iteration an object needs to implement the iterator protocol by providing the __iter__ and __next__ dunder methods.

* Class-based iterators are only one way to write iterable objects in Python. Also consider generators and generator expressions.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Generators
* Generators are a tricky subject in Python. With this tutorial you’ll make the leap from class-based iterators to using generator functions and the “yield” 
statement in no time.
* Generator functions are syntactic sugar for writing objects that support the iterator protocol. Generators abstract away much of the boilerplate code 
needed when writing class-based iterators.
* The yield statement allows you to temporarily suspend execution of a generator function and to pass back values from it.
* Generators start raising StopIteration exceptions after control flow leaves the generator function by any means other than a yield statement.
























































