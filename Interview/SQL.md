# SQL Interview Questions

### What is index. What are the type of Index?

### What is cross Join?

### What is the difference between Union and Union All?

### What is the difference between primary key and unique key?
> A primary key is a key that uniquely identifies each record in a table but cannot store NULL values. In contrast, a unique key prevents duplicate values in a column and can store NULL values.
> A table can have multiple unique key but it can have only one primary key.

### What is foreign key?
> A `FOREIGN KEY` is a field (or collection of fields) in one table, that refers to the `PRIMARY KEY` in another table.

### What is the difference between function and stored procedure?
| Functions |	Procedures
--- | ---
A function has a return type and returns a value.	| A procedure does not have a return type. But it returns values using the OUT parameters.
You cannot use a function with Data Manipulation queries. Only Select queries are allowed in functions.	| You can use DML queries such as insert, update, select etc… with procedures.
A function does not allow output parameters |	A procedure allows both input and output parameters
You cannot manage transactions inside a function |	You can manage transactions inside a procedure
You cannot call stored procedures from a function	| You can call a function from a stored procedure
You can call a function using a select statement | You cannot call a procedure using select statements

### JOIN 2 table?

```SQL
SELECT * FROM Student st
JOIN School sc ON st.SchoolId = sc.Id
WHERE Percentage > 30
```

### What is the difference between local table and global table ?

### What is View in SQL?
> View is the virtual table which doesn't take any memory.

### Types of lock in SQL?
>

### How to get the inserted id of a table?
>


