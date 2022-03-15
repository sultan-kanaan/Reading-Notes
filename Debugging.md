## Exception Handling & Debugging
## Debugging
>Debugging means to run your code step by step in a debugging tool like Visual Studio, to find the exact point where you made a programming mistake.


In Visual Studio, you enter debugging mode by using F5 or the Start Debugging button .

## Exception Handling

>Exception handling statements

`throw`

`try-catch`

`try-finally`

`try-catch-finally`

## Example

```
   public static void Main()
    {
        try
        {
            using (StreamReader sr = File.OpenText("data.txt"))
            {
                Console.WriteLine($"The first line of this file is {sr.ReadLine()}");
            }
        }
        catch (FileNotFoundException e)
        {
            Console.WriteLine($"The file was not found: '{e}'");
        }
```
