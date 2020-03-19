# Classes & Object

## Classes

#### Declaring A Class

You can declare a class in C# by using the `class` keyword, followed by a unique name for the class:

```
public class NewClass
{
    // Class properties, methods, etc here...
}
```

In the above example we declared the class access modifier as `public`, meaning that anyone can create an instance of this class. We then gave it the unique name of `NewClass`. We can define any properties, methods, constructors, etc that we want to fall within our class. These are called _**members**_.

#### Objects & Instances

Classes and objects in C# are same-same, but different. An object is actually an _**instance**_ of a class:

```
NewClass newObject = new NewClass();
```

Here we have created a new object by the name of `newObject` that is of the type `NewClass`. We then assign it the value of a new instance of the `NewClass` class we created previously.

#### Inheritance & Extending A Class

Classes in C# support _inheritance_, wherein we can extend a class when creating a new class:

```
public class NewClass : OldClass
{
    // OldClass properties, methods, etc are inherited and accessible.
    // NewClass properties, methods, etc go here.
}
```

In our example above, we declared the class `NewClass`, but this time we also declared that it has a base class called `OldClass`. This allows our `NewClass` class to have access to all of the members of `OldClass` with exception to the constructors.

A class can only declare one base class, however, that base class could potentially have declared a base class, and so on. This may allow our class to indirectly inherit any members within those base classes further up the pipeline (so to speak).

## Constructors

Whenever a class is created its constructor is called. Constructors enable us to set default values, limit instantiation, and more for our classes.

#### Constructor Syntax

A constructor is a method with the same name as its class name. Its method signature only includes the method name, and its parameter list, there is no return type. Example:

```
public class Person
{
    private string last;
    private string first;

    public Person(string lastName, string firstName)
    {
        last = lastName;
        first = firstName;
    }

    // Remaining Person members...
}
```
