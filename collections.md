# Collections

## What Are Collections?

Collections are a more flexible way to group objects together, as opposed to using arrays.

Where arrays are fixed in length, collections and grow or shrink dynamically.

For some collections, you can even assign a key to objects, so that you can quickly grab that object by its key.

## Generic Collections

If your collection only contains objects of one data type, you can use a class from the `System.Collections.Generic` namespace. Generic collections enforce type safety, meaning that you can only add one data type to it. This also means that when you retrieve an object from a generic collection you do not have to determine its type or try to convert it.

## Generic List Example

The following example creates a List of strings and then iterates through that list:

```
var salmons = new List<string>();
salmons.Add("chinook");
salmons.Add("coho");
salmons.Add("pink");
salmons.Add("sockeye");

foreach (var salmon in salmons)
{
    Console.WriteLine(salmon);
}

// Output:
// chinook
// coho
// pink
// sockeye
```
