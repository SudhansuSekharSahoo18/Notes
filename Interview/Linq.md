### Join in LINQ?

``` C#
var list = students.Join(schools, 
            student => student.SchoolId, 
            school => school.Id, 
            (student, school) => new
            {
                StudentName = student.Name,
                school.SchoolName
            });
```

### What is the difference between First() and FirstOrDefault()?
> In the collection if the search element is not present then First() will throw the exception where FirstOrDefault() will return `null` value.

### What is the difference between Select() and SelectMany()?
> Select and SelectMany are projection operators. A select operator is used to select value from a collection and SelectMany operator is used to selecting values from a collection of collection i.e. nested collection.

```C#
 // Query using Select()
 IEnumerable<List<String>> resultSelect = employees.Select(e=> e.Skills);

 // Query using SelectMany()
 IEnumerable<string> resultSelectMany = employees.SelectMany(emp => emp.Skills);
```

### Projection in LINQ?
> Projection refers to the operation of transforming an object into a new form that often consists only of those properties that will be subsequently used. By using projection, you can construct a new type that is built from each object. You can project a property and perform a mathematical function on it. You can also project the original object without changing it.
