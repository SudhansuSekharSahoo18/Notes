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
>

### Projection in LINQ?
> Projection refers to the operation of transforming an object into a new form that often consists only of those properties that will be subsequently used. By using projection, you can construct a new type that is built from each object. You can project a property and perform a mathematical function on it. You can also project the original object without changing it.
