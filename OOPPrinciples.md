# OOP Principles

## Inheritance
> derive types to create more specialized behavior

In C#, it is possible to inherit fields and methods from one class to another. We group the "inheritance concept" into two categories:

* Derived Class (child) - the class that inherits from another class.
* Base Class (parent) - the class being inherited from.

**To inherit from a class, use the `:` symbol.**

Example

```
class Vehicle  // base class (parent) 
{
  public string brand = "Ford";  // Vehicle field
  public void honk()             // Vehicle method 
  {                    
    Console.WriteLine("Tuut, tuut!");
  }
}

class Car : Vehicle  // derived class (child)
{
  public string modelName = "Mustang";  // Car field
}

class Program
{
  static void Main(string[] args)
  {
    // Create a myCar object
    Car myCar = new Car();

    // Call the honk() method (From the Vehicle class) on the myCar object
    myCar.honk();

    // Display the value of the brand field (from the Vehicle class) and the value of the modelName from the Car class
    Console.WriteLine(myCar.brand + " " + myCar.modelName);
  }
}
```

## Abstract 


The `abstract` keyword is used for classes and methods:

* Abstract class: is a restricted class that cannot be used to create objects (to access it, it must be inherited from another class).

* Abstract method: can only be used in an abstract class, and it does not have a body. The body is provided by the derived class (inherited from).

## Polymorphism
`Polymorphism` means "many forms", and it occurs when we have many classes that are related to each other by inheritance.

For example, think of a base class called Animal that has a method called animalSound(). Derived classes of Animals could be Pigs, Cats, Dogs, Birds - And they also have their own implementation of an animal sound (the pig oinks, and the cat meows, etc.):
```
class Animal  // Base class (parent) 
{
  public void animalSound() 
  {
    Console.WriteLine("The animal makes a sound");
  }
}

class Pig : Animal  // Derived class (child) 
{
  public void animalSound() 
  {
    Console.WriteLine("The pig says: wee wee");
  }
}

class Dog : Animal  // Derived class (child) 
{
  public void animalSound() 
  {
    Console.WriteLine("The dog says: bow wow");
  }
}
```



