### What is the difference between `dynamic` and `var`?

### What is the difference between IEnumerable and IQueryable?

### Extension method in C# ?

> In C#, the extension method concept allows you to add new methods in the existing class or in the structure without modifying the source code of the original type and you do not require any kind of special permission from the original type and there is no need to re-compile the original type.

```C#
static class StringHelper {
  
    public static bool IsNullOrEmpty(this string str)
    {
        return str.IsNullOrEmpty(str);
    }
  
    // Method 5
    public static string Append(this string str, string text)
    {
        return str + text;
    }
}
```

### Difference between POST, PUT, and PATCH?

### What is Generic?
> Generics in C# is a feature that allows for the creation of reusable code by creating parameterized types. In simple terms, it enables us to create classes, interfaces, and methods that work with different data types without having to define the data type explicitly.

### What are delegates?
> Delegates are type-safe function pointers. It references methods with a particular parameter list and return type and then calls the method in a program for execution when it is needed.

```C#
public class A
{
    public delegate void addnum(int a, int b);
            
    public void sum(int a, int b)
    {
        Console.WriteLine(a + " + " + b + " = " + a+b);
    }

    public static void Main(String []args)
    {
        A obj = new A();
        addnum del_obj1 = new addnum(obj.sum);
        del_obj1(100, 40);
        // del_obj1.Invoke(100, 40);
    }
}
``` 

### Multicasting of delegates?
> Multicasting of delegate is an extension of the normal delegate(sometimes termed as Single Cast Delegate). It helps the user to point more than one method in a single call.

```C#
using System;
 
class rectangle
{
public delegate void rectDelegate(double height, double width);
 
    public void area(double height, double width)
    {
        Console.WriteLine("Area is: {0}", (width * height));
    }
  
    public void perimeter(double height, double width)
    {
        Console.WriteLine("Perimeter is: {0} ", 2 * (width + height));
    }
  
public static void Main(String []args)
{
    rectangle rect = new rectangle();
    rectDelegate rectdele = new rectDelegate(rect.area);
    rectdele += rect.perimeter;
    rectdele.Invoke(6.3, 4.2);
}
}
```
```
Area is: 26.46
Perimeter is: 21 
```

### What is Entity Framework?

### Explain garbage collector?

### What is Function overloading and function overriding?

### How to call base class constructor?

### What is reflection ?
> Reflection is the process of describing the metadata of types, methods and fields in a code. The namespace System.Reflection enables you to obtain data about the loaded assemblies, the elements within them like classes, methods and value types.