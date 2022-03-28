# Interfaces
>An `interface` contains definitions for a group of related functionalities that a non-abstract class or a struct must implement.


* Like abstract classes, interfaces cannot be used to create objects (in the example above, it is not possible to * create an "IAnimal" object in the Program class)
* Interface methods do not have a body - the body is provided by the "implement" class
* On implementation of an interface, you must override all of its methods
* Interfaces can contain properties and methods, but not fields/variables
* Interface members are by default abstract and public
* An interface cannot contain a constructor (as it cannot be used to create objects)


## Why And When To Use Interfaces?
1) To achieve security - hide certain details and only show the important details of an object (interface).

2) C# does not support "multiple inheritance" (a class can only inherit from one base class). However, it can be achieved with interfaces, because the class can implement multiple interfaces. Note: To implement multiple interfaces, separate them with a comma (see example below).


Example :
```
interface Animal 
{
  void animalSound(); // interface method (does not have a body)
  void run(); // interface method (does not have a body)
}
```

```
interface IPoint
{
   // Property signatures:
   int X
   {
      get;
      set;
   }

   int Y
   {
      get;
      set;
   }

   double Distance
   {
       get;
   }
}

class Point : IPoint
{
   // Constructor:
   public Point(int x, int y)
   {
      X = x;
      Y = y;
   }

   // Property implementation:
   public int X { get; set; }

   public int Y { get; set; }

   // Property implementation
   public double Distance =>
      Math.Sqrt(X * X + Y * Y);

}

class MainClass
{
   static void PrintPoint(IPoint p)
   {
      Console.WriteLine("x={0}, y={1}", p.X, p.Y);
   }

   static void Main()
   {
      IPoint p = new Point(2, 3);
      Console.Write("My Point: ");
      PrintPoint(p);
   }
}
// Output: My Point: x=2, y=3
```