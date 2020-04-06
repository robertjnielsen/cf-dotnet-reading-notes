# SOLID Code

## What Is SOLID Code?

_SOLID_ is an acronym which we'll cover in a little bit of depth as we go forward here, but suffice to say that it is a method of writing code that is clean, purposeful, reuasable, and lends itself well to Test-Driven Development.

Now, let's break down what SOLID is:
- **S**ingle Responsibility Principle
- **O**pen/Close Principle
- **L**iskov Substitue Principle
- **I**nterface Segregation Principle
- **D**ependency Inversion Principle

## Single Responsibility Principle

The Single Responsibility Principle is something we're all probably familiar with. Succinctly put each of our classes, methods, etc should really only be built around one singular purpose, and should be paired down as much as possible to make use of only what is needed to accomplish that purpose.

## Open/Close Principle

The Open/Close Principle states that software should be open to extension, but closed to modification. Making good use of _Inheritance_, _Polymorphism_ and _Encapsulation_ help create code that is less prone to bugs and errors, while still giving the option to extend that code for tackle varying situations / purposes.

## Liskov Substitution Principle

The Liskov Substitution Principle states that an object in your application should be able to be replaced with a type derived from it, without breaking the application. Think of this as your code intending to accept an `Animal` super class, but being able to pass a `Cow` derived class in it's place. This works because `Cow` is derived _from_ the `Animal` class, and thus _is itself_ an `Animal`.

## Interface Segregation Principle

The Interface Segregation Principle states that clients should not be forced to rely on any interfaces that they may not make use of. Imagine if Visual Studio did not give you different Project types to create, and instead _every_ option for _every_ project type was baked into the interface all at once. You wouldn't be able to find anything or know where to go to get anything done. It's the same with programming our interfaces. Creating many smaller, fine-tuned interfaces for our classes enables us to use what we need from where we need, and also allows TDD to move forward easier by implementing only the interfaces we need for each test.

## Dependency Inversion Principle

The Dependency Inversion Principle states that code should depend upon abstractions and not concrete implementations. An example given is a service that connects to a database. You could have varied concrete instances to connect to different database types or environments, but if you rely on one, then you are locked in to that one. However if you have your service dependent upon an abstraction, then it doesn't matter what type of database you utilize, you can work with any of them.

## Wrapping It Up

SOLID makes a _little_ more sense to me now, though I've only just scratched the surface. Hopefully through more time working with thise principles in mind it will start to **click**.
