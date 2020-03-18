# `System.IO`

In the .NET framework, the `System.IO` namespace allows reading and writing from files and data streams (among other methods).

## Files and Directories
The various types in the `System.IO` namespace allow interaction with files and directories.

Examples:

`File` - static methods for creating, copying, deleting, moving, and opening files.

`FileInfo` - instance methods similar to `File`.

`Directory` - static methods for creating, moving and enumerating through directories and subdirectories.

`DirectoryInfo` - instance methods similar to `Directory`.

`Path` - methods and properties for processing directory strings in a cross-platform manner.

## Others

The `System.IO` namespace also has types for several other methods and operations, to include:

- Streams
- Readers and Writers
- Asynchronous I/O Operations
- Compression
- Isolated Storage
- And more.

## Example: Writing Text to a File

We will go ahead and use an example provide by the [Microsoft Documentation](https://docs.microsoft.com/en-us/dotnet/standard/io/how-to-write-text-to-a-file) to write some sample text to a new file.

```
using System;
using System.IO;

class Program
{
    static void Main(string[] args)
    {
        // Create a string array with the lines of
        // text we want in our file.
        string[] lines = { "First line", "Second line", "Third line" };

        // Set a variable to the "Documents" path.
        string docPath = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);

        // Write the string array to a new file named "WriteLines.txt".
        using (StreamWrite outputFile = new StreamWriter(Path.Combine(docPath, "WriteLines.txt")))
        {
            foreach (string line in lines)
            {
                outputFile.WriteLine(line);
            }
        }
    }
}
```

This example uses the StreamWriter type to create a new file named **WriteLines.txt** in the **MyDocuments** directory, which was stored in the string variable defined as `docPath`.

It then writes the strings stored in the string array titled `lines` by using a `foreach` method, and the `outputFile.WriteLine` method.