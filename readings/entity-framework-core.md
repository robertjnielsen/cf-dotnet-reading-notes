# Entity Framework Core

## What Is EF Core?

[Entity Framework (EF) Core is a lightweight, extensible, open source and cross-platform version of the popular Entity Framework data access technology.](https://docs.microsoft.com/en-us/ef/core/)

EF Core acts as an **_object relational mapper (ORM)_** for the .NET framework, allowing developers to work with a database using .NET objects, and eliminating the need to work with the database directly.

## Database Providers

To utilize EF Core, you have to install a NuGet package for the database provider. This allows you to work with EF Core and your targeted database environment.

## Models

EF Core works with models in the form of entity classes. This can be as simple as creating a class to represent _(ahem... model)_ the data that you will be working with in your database / application.

The example given by the [Microsoft Docs](https://docs.microsoft.com/en-us/aspnet/core/data/ef-mvc/intro?view=aspnetcore-3.1#the-student-entity) is:

```
public class Student
{
    public int ID { get; set; }
    public string LastName { get; set; }
    public string FirstMidName { get; set; }
    public DateTime EnrollmentDate { get; set; }

    public ICollection<Enrollment> Enrollments { get; set; }
}
```

Looking at this model, we see that it has an `ID` property. This will become the **Primary Key** column of the database table that will represent this class.

We also have three more columns being established with the `LastName`, `FirstMidName` and `EnrollmentDate` properties.

The final property, `Enrollments` is a collection. This makes it a **Navigation Property** for our model. This property will hold all of the `Enrollment` data in our database associated with each `Student`, which is why it is a collection.
