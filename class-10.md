# Read:10 Summary
## Stacks and Queues
* A `stack` is :  a data structure that consists of Nodes. Each Node references the next Node in the stack, but does not reference its previous.
* Common terminology for a stack is : 
  * `Push` : Nodes or items that are put into the stack are pushed

  * `Pop`: Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.

  * `Top` :  This is the top of the stack.

  * `Peek` : When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.

  * `IsEmpty` : returns true when stack is empty otherwise returns false.
  
 
 ***Stacks follow these concepts:***
  
    * `FILO`(First In Last Out) : This means that the first item added in the stack will be the last item popped out of the stack.
    * `LIFO`(Last In First Out) : This means that the last item added to the stack will be the first item popped out of the stack
    
* Pushing a Node onto a stack will always be an `O(1)` operation. This is because it takes the same amount of time no matter how many
   Nodes (n) you have in the stack.
* When adding a Node, you push it into the stack by assigning it as the new top, with its next property equal to the original top.

* `ALOGORITHM push(value)`
* ` INPUT <-- value to add, wrapped in Node internally`
* `OUTPUT <-- none`
* `node = new Node(value)`
* `node.next <-- Top`
* `top <-- Node`
* Popping a Node off a stack is the action of removing a Node from the top. When conducting a pop, the top Node will be re-assigned to the Node that 
lives below and the top Node is returned to the user.
* `ALGORITHM pop()`

* `Node temp <-- top`
* `top <-- top.next`
* `temp.next <-- null`
*`ret urn temp.value`
* When conducting a peek, you will only be inspecting the top Node of the stack.
### What is a Queue ?
***Common terminology for a queue is:***
  * `Enqueue` - Nodes or items that are added to the queue.

  * `Dequeue` - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.

  * `Front` - This is the front/first Node of the queue.

  * `Rear` - This is the rear/last Node of the queue.

  * `Peek` - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.

  * `IsEmpty `- returns true when queue is empty otherwise returns false.

* `FIFO` (First In First Out) : This means that the first item in the queue will be the first item out of the queue.
* `LILO` : Last In Last Out

  








    



