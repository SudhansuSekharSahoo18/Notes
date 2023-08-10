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
