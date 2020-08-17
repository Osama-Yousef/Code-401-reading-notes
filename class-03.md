# Read:03 summary 
## Reading and Writing Files in Python

### What Is a File?
*  is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text
file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.
* file systems are composed of three main parts:
  * Header: metadata about the contents of the file (file name, size, type, and so on)
  * Data: contents of the file as written by the creator or editor
  * End of file (EOF): special character that indicates the end of the file

* The `file path`: is a string that represents the location of a file. It’s broken up into three major parts:
  * `Folder Path`: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)

  * `File Name`: the actual name of the file

  * `Extension`: the end of the file path pre-pended with a period (.) used to indicate the file type

### Opening and Closing a File in Python

* `open()` has a single required argument that is the path to the file. open() has a single return, the file object:

* for example : `file = open('dog_breeds.txt')`

* there are two ways that you can use to ensure that a file is closed properly :
  * use the `try-finally` block:
  * use the with statement
* There are three different categories of file objects:
  * Text files

  * Buffered binary files

  * Raw binary files

-----------------------------------------------------------------------------------------------------------------------------
## Python Exceptions: An Introduction

***A Python program terminates as soon as it encounters an error. In Python, an error can be a syntax error or an exception***
### Exceptions versus Syntax Errors

* `Syntax errors` occur when the parser detects an incorrect statement.
* `exception error`: This type of error occurs whenever syntactically correct Python code results in an error.
### Raising an Exception
 * We can use `raise` to throw an exception if a condition occurs. The statement can be complemented with a custom exception.

### The AssertionError Exception
* Instead of waiting for a program to crash midway, you can also start by making an assertion in Python. We `assert` that a certain condition
is met. If this condition turns out to be `True`, then that is excellent! The program can continue. If the condition turns out to be `False`, you can
have the program throw an `AssertionError` exception.
### The try and except Block: Handling Exceptions
* The` try` and `except` block in Python is used to catch and handle exceptions. Python executes code following the `try` statement as a “normal” part of
the program. The code that follows the `except` statement is the program’s response to any exceptions in the preceding `try` clause.
***useful notes about `try` and `except`
  * A `try` clause is executed up until the point where the first exception is encountered.

  * Inside the `except` clause, or the exception handler, you determine how the program responds to the exception.
  * You can anticipate multiple exceptions and differentiate how the program should respond to them.

### The `else` Clause
* In Python, using the `else` statement, you can instruct a program to execute a certain block of code only in the absence of exceptions.
### Cleaning Up After Using `finally`
* Imagine that you always had to implement some sort of action to clean up after executing your code. Python enables you
to do so using the `finally` clause.

----------------------------------------------------------------------------------------------------------------------






  




















