# Linked Lists
>A Linked List is a sequence of `Nodes` that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the `next` Node in the link.

## types of Linked List:
* Singly Linked List.

  Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.

![](./img/Singly-Linked-List1.png)

* Doubly Linked List.

  Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.

![](./img/Doubly-Linked-List.png)

* Circular Linked List.

  Last item contains link of the first element as next and the first element has a link to the last element as previous.
![](./img/Circular-Linked-List.png)


## Basic Operations
Following are the basic operations supported by a list :

* `Insertion` − Adds an element at the beginning of the list.

* `Deletion` − Deletes an element at the beginning of the list.

* `Display` − Displays the complete list.

* `Search` − Searches an element using the given key.

* `Delete` − Deletes an element using the given key.


## Add End of the link list
```
public void AddEnd(int value)
        {
            Node item = new Node(value);
            if (Head == null)
            {
                Head = item;
                Tail = item;
            }
            else
            {
                Tail.Next = item;
                Tail = item;
            }
```

## Add First  of the link list
```
public void AddFirst(int value)
        {
            Node item = new Node(value);
            if(Head == null)
            {
                Head = item;
                Tail = item;
            }
            else
            {
                item.Next = Head;
                Head = item;
            }
```            
## Add anyware of the link list 

```
 public void AddAfter(int value, int position)
        {
            Node current = Head;
            for (int i = 0; i < position; i++)
            {
                current = current.Next;
                if (current == null)
                {
                    Console.WriteLine("out of range!");
                    return;
                }
            }
            Node NewNode = new Node(value);
            NewNode.Next = current.Next;
            current.Next = NewNode;

        }
```        
