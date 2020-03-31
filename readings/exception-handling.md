# Exception Handling
When writing code for applications or programs, we need to take in to consideration errors that may occur during runtime.

One way to handle this is with a method of **Exception Handling** that we call a _**try/catch**_ block.

A try/catch block allows us to create a `try` code block, and place the code within it that we want to run, but that we also know may generate one or more errors.

Example:  
```
try
{
    DoAThing(withAThing)
    {
        thing = makeStuffHappen;
    }
}
```
We know that sometimes things go wrong, and errors are thrown around like a bad juggler in a cheap circus. That's why we utilize the `catch` code blocks to handle these exceptions.

Example:
```
catch (ThingWentWrong e)
{
    Console.WriteLine($"This happened: {e}");
}
```
This allows us to capture the error stored as `e` and print it out to the console.

Any errors that are thrown that are not caught with `catch` code blocks are caught by the _**Common Language Runtime (CLR)**_, which may handle the result by either;
- Displaying a **Debug** dialog box,
- Stopping execution of the program and displaying a dialog box with exception information,
- Or printint out an error to the standard error output stream.

All in all, the above example put together would look like this:

```
try
{
    DoAThing(withAThing)
    {
        thing = makeStuffHappen;
    }
}
catch (ThingWentWrong e)
{
    Console.WriteLine($"This happened: {e}");
}
```
