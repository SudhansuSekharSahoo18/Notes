
### Join in LINQ ?

var list = students.Join(schools, 
            student => student.SchoolId, 
            school => school.Id, 
            (student, school) => new
            {
                StudentName = student.Name,
                school.SchoolName
            });

### Difference between POST, PUT and PATCH ?

