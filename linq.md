# LINQ

## What Is LINQ?

_**Language Integrated Query (or LINQ)**_ is a set of technologies in C# and .NET that allow developers to query a data set.

A query is an expression that retrieves data from a data source. Queries are usually expressed in some form of specific query language, dependant updon the data source.

LINQ gives us a consistent model for working with data across varying data sources and formats.

## Three Parts Of A Query

LINQ queries operate with three distinct parts:

1. Obtain the data source.
2. Create the query.
3. Execute the query.

The following example ([shamelessly ripped from MS Docs](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries)) shows how these three steps work together:

```
class IntroToLINQ
{
    static void Main()
    {
        // 1. Data source
        int[] Numbers = new int[7] { 0, 1, 2, 3, 4, 5, 6 };
        
        // 2. Create the query
        // numQuery is an IEnumarable<int>
        var numQuery =
            from num in numbers
            where (num % 2) == 0
            select num;

        // 3. Execute query
        foreach (int num in numQuery)
        {
            Console.Write("{0,1} ", num);
        }
    }
}
```
