
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

### 

