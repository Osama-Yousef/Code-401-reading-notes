# Read:05 Summary 
## Linked lists

* `Linked List ` : is a sequence of `Nodes` that are connected/linked to each other. The most defining feature of a Linked List is that 
each `Node` references the next `Node` in the link.
* There are two types of Linked List :
  * Singly 
  * Doubly
* `Node` : is the individual items/links that live in a linked list. Each node contains the data for each link.
* `Singly` : refers to the number of references the node has. A Singly linked list means that there is only one reference, and the 
reference points to the `Next` node in a linked list.
* `Doubly` : refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the
`Next` and `Previous` node.
* `Next` : This property contains the reference to the next node.
* `Head` : This property contains the reference to the first node in a linked list.
***The best way to traverse through a linked list is using of a while() loop not forEach or for loop***

* `Current`: is node that will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.
***When constructing your code, a few things to keep in mind :***

  * When making your `Node` class, consider requiring a value to be passed in to require that each node has a value.


  * When making a Linked List, you may want to require that at least one node gets passed in upon instantiation. This first node is 
  what your `Head` and `Current` will point too.
  
  --------------------------------------------------------------------------------------------------------------------------------------
* `linear data structures` : which means that there is a sequence and an order to how they are constructed and traversed. 
* `non-linear data structures` : items don’t have to be arranged in order, which means that we could traverse the data structure non-sequentially.
  
* The fundamental difference between ***arrays*** and ***linked lists*** is that arrays are ***static data structures***, while linked lists are
  ***dynamic data structures.***
  
* `linked list` can be small or huge, but no matter the size, the parts that make it up are actually fairly simple. A linked list is made up of
  a series of nodes, which are the elements of the list.
  
***`Singly linked lists` : are the simplest type of linked list***
  
* `Doubly linked list` : there are two references contained within each node: a reference to the `next` node, as well as the `previous` node
-----------------------------------------------------------------------------------------------------------------------------------------------------
## Big O Notation
* is a way of evaluating the performance of an algorithm.

* `Big O Notation` :  takes into account: the speed and efficiency with which something functions when its input grows to be any (crazy big!) size.

* `O` (referred to as just “O” or sometimes as “order”), and a variable `n`, where n is the size of the input 
* `O(1) function` : takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always
take the same amount of time and memory to run our algorithm.
* `O(n)` :  function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and 
time that we need to run that algorithm grows linearly.

* `O(n²) function` : which clearly takes exponentially more time and memory the more elements that you have. It’s pretty safe to say that
we want to avoid O(n²) algorithms, just from looking at that crazy red line!

***a linked list is usually efficient when it comes to adding and removing most elements, but can be very slow to search and find a single element***

### When we need arrays OR linked lists ?
* arrays : if you do know the size of the list , you need random access to elements or want to iterate quickly
* linked lists : if you dont know the size of the list ,and mostly want to add or remove things quickly without random access
 

















