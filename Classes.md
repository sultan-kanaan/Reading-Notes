# Classes & Memory Management

#### A type that is defined as a class is a `reference type`. At run time, when you declare a variable of a reference type, the variable contains the value null until you explicitly create an instance of the class by using the new operator, or assign it an object of a compatible type that may have been created elsewhere

example:
```
MyClass mc = new MyClass();

MyClass mc2 = mc;
```

## Declaring Classes
#### Classes are declared by using the `class` keyword followed by a unique identifier
example:
```
public class Customer
{

}
```

## Creating objects

#### Objects can be created by using the new keyword followed by the name of the class that the object will be based on
example:
```
Customer object1 = new Customer();
```
 `object1` is a reference to an object that is based on `Customer`. This reference refers to the new object but does not contain the object data itself.

 ## Class inheritance

#### When you create a class, you can inherit from any other class that is not defined as sealed, and other classes can inherit from your class and override class virtual methods. Furthermore, you can implement one or more interfaces.
example:
```
public class Manager : Employee
{

}
```
#### A class in C# can only directly inherit from one base class. However, because a base class may itself inherit from another class, a class may indirectly inherit multiple base classes. Furthermore, a class can directly implement one or more interfaces.


## Constructor

#### A `constructor` is a method whose name is the same as the name of its type. Its method signature includes only an optional access modifier, the method name and its parameter list; it does not include a return type.
example:
```
public class Person
{
   private string last;
   private string first;

   public Person(string lastName, string firstName)
   {
      last = lastName;
      first = firstName;
   }

}
```

## Properties

>A property is a member that provides a flexible mechanism to read, write, or compute the value of a private field. Properties can be used as if they are public data members, but they are actually special methods called accessors. This enables data to be accessed easily and still helps promote the safety and flexibility of methods.

* Properties enable a class to expose a public way of getting and setting values, while hiding implementation or verification code.

* `get`property accessor is used to return the property value.

* `set` property accessor is used to assign a new value.

* The `value` keyword is used to define the value being assigned by the `set`.

example:
```
using System;

class TimePeriod
{
   private double _seconds;

   public double Hours
   {
       get { return _seconds / 3600; }
       set {
          if (value < 0 || value > 24)
             throw new ArgumentOutOfRangeException(
                   $"{nameof(value)} must be between 0 and 24.");

          _seconds = value * 3600;
       }
   }
}

class Program
{
   static void Main()
   {
       TimePeriod t = new TimePeriod();
       t.Hours = 24;
       Console.WriteLine($"Time in hours: {t.Hours}");
   }
}

```





