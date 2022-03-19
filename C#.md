# The history of C# :

>we are in C# version 10

### C# 10 adds the following features and enhancements to the C# language:

* #### Record structs
* #### Improvements of structure types
* #### Interpolated string handlers
* #### global using directives
* #### File-scoped namespace declaration
* #### Extended property patterns
* #### Improvements on lambda expressions
* #### Allow const interpolated strings
* #### Record types can seal ToString()
* #### Improved definite assignment
* #### Allow both assignment and declaration in the same deconstruction
* #### Allow AsyncMethodBuilder attribute on methods
* #### CallerArgumentExpression attribute
* #### Enhanced #line pragma

>C# 10 continues work on themes of removing ceremony, separating data from algorithms, and improved performance for the .NET Runtime.

# .Net Core Guide :
* .NET is a free, cross-platform, open source developer platform for building many different types of applications.

* With .NET, you can use multiple languages, editors, and libraries to build for web, mobile, desktop, games, and IoT.

>.NET is a free, open-source development platform for building many kinds of apps, such as:

- Web apps, web APIs, and microservices
- Serverless functions in the cloud
- Cloud native apps
- Mobile apps
- Desktop apps
   1. Windows WPF
   2. Windows Forms
   3. Universal Windows Platform (UWP)
- Games
- Internet of Things (IoT)
- Machine learning
- Console apps
- Windows services

## .NET supports three programming languages:
  * C#
  * F#
  * Visual Basic

 ### Common Language Runtime (CLR)
 .NET provides a run-time environment, called the common language runtime, that runs the code and provides services that make the development process easier.

### managed code
When working with .NET, you will often encounter the term "managed code". This document will explain what this term means and additional information around it.

 ## "Hello, World" program
 ```
 using System;

class Hello
{
    static void Main()
    {
        Console.WriteLine("Hello, World");
    }
}
```
## Value types
- Signed integral: `sbyte`, `short`, `int`, `long`
- Unsigned integral: `byte`, `ushort`, `uint`, `ulong`
- Unicode characters: `char`, which represents a UTF-16 code unit
- IEEE binary floating-point: `float`, `double`
- High-precision decimal floating-point: `decimal`
- Boolean: `bool`, which represents Boolean values—values that are either true or false
- Unicode strings: `string`

## C# Arrays
>Single-Dimensional Arrays
```
int[] array = new int[5];
```

>Multidimensional Arrays
```
int[,] array = new int[4, 2];
```
>Jagged Arrays
```
int[][] jaggedArray = new int[3][];
```


