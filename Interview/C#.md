
### Join in LINQ?

```C#
var list = students.Join(schools, 
            student => student.SchoolId, 
            school => school.Id, 
            (student, school) => new
            {
                StudentName = student.Name,
                school.SchoolName
            });
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

```

```
