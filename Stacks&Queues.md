# Stacks and Queues

## Stack
A `stack`is a data structure that consists of `Nodes`. Each `Node` references the next Node in the stack, but does not reference its previous.

>Common terminology for a stack is :
* `Push` - Nodes or items that are put into the stack are pushed
* `Pop` - Nodes or items that are removed from the stack are popped. When you attempt to pop an empty stack an exception will be raised.
* `Top` - This is the top of the stack.
* `Peek` - When you peek you will view the value of the top Node in the stack. When you attempt to peek an empty stack an exception will be raised.
* `IsEmpty` - returns true when stack is empty otherwise returns false.


## Stack Visualization
![](./img/Stack.png)

* Push O(1)
* Pop O(1)
* Peek O(1)
* IsEmpty O(1)


## Queue
>Common terminology for a queue is


* `Enqueue` - Nodes or items that are added to the queue.
* `Dequeue` - Nodes or items that are removed from the queue. If called when the queue is empty an exception will be raised.
* `Front` - This is the front/first Node of the queue.
* `Rear` - This is the rear/last Node of the queue.
* `Peek` - When you peek you will view the value of the front Node in the queue. If called when the queue is empty an exception will be raised.
* `IsEmpty` - returns true when queue is empty otherwise returns false.

## Queue Visualization
![](./img/Queue.png)

* Enqueue O(1)
* Dequeue O(1)
* Peek O(1)
* IsEmpty O(1)





