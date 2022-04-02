# Collections & Enums

## Collections
>There are two ways to group objects:

* by creating arrays of objects
* by creating collections of objects.

#### Collections provide a more flexible way to work with groups of objects.


## Kinds of Collections :

* System.Collections.Generic 

* System.Collections.Concurrent 

* System.Collections 

## Using a Simple Collection
The examples in this section use the generic List<T> class, which enables you to work with a strongly typed list of objects.

```
// Create a list of strings.
var salmons = new List<string>();
salmons.Add("chinook");
salmons.Add("coho");
salmons.Add("pink");
salmons.Add("sockeye");

// Iterate through the list.
foreach (var salmon in salmons)
{
    Console.Write(salmon + " ");
}
// Output: chinook coho pink sockeye
```

frequently Types:
* ArrayList
* Hashtable
* Queue
* Stack


## Using a Generic Collection
A generic collection is useful when every item in the collection has the same data type. A generic collection enforces strong typing by allowing only the desired data type to be added

frequently Types:
* Dictionary<TKey,TValue>
* List<T>
* Queue<T>
* SortedList<TKey,TValue>
* Stack<T>


## Using a Concurrent Collection
provide efficient thread-safe operations for accessing collection items from multiple threads.


frequently Types:
* BlockingCollection<T>
* ConcurrentDictionary<TKey,TValue>
* ConcurrentQueue<T>
* ConcurrentStack<T>

# enum type
To define an enumeration type, use the `enum` keyword and specify the names of enum members

example:
```
enum Season
{
    Spring,
    Summer,
    Autumn,
    Winter
}
```
> By default, the associated constant values of enum members are of type int; they start with zero and increase by one following the definition text order.





