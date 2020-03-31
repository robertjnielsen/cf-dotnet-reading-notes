# Interfaces

## What Are Interfaces?

An **Interface** is similar to a class, but provides a specification for its members instead of an implementation. This means that they are essentially templates, and cannot be instantiated.

## Some Key Differences

Some notable things that seperate interfaces from classes is that all interface members are _implicitly abstract_. Whereas in a class, you can provide both abstract and concrete members, an interface does not give you that option.

Also, where a class can only extend and inherit from a single base class, classes can implement multiple interfaces.

## Declaration

An interface can be declared as such:
```
public interface ISampleInterface
{
    // some members here
}
```

## Implementing An Interface

An interface can be implemented much like extending a class, as such:
```
public class SampleClass : ISampleInterface
{
    // class members here
}
```

## Extending An Interface

Interfaces can also derive from other interfaces, like so:
```
public interface IAnotherInterface : ISampleInterface
{
    // members go here
}
```

## Access

Interface members are always implicitly public and cannot declare an access modifier.
