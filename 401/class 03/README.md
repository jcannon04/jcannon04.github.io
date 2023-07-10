**Files and directories:** Covers interactions with files and directories, including properties, collections, and search criteria.

**Streams:** Introduces the concept of streams, which are sequences of bytes used for reading from and writing to different storage mediums.

**Readers and writers:** Describes types for reading encoded characters from streams and writing them back, including binary and text-based operations.

**Asynchronous I/O operations:** Highlights the benefits of performing I/O operations asynchronously for resource-intensive tasks in order to maintain application responsiveness.

**Compression:** Explains the process of reducing file size and decompression, along with relevant classes for compressing and decompressing files and streams.

**Isolated storage:** Discusses a data storage mechanism for isolating and securing application data, particularly useful when access to user files is restricted.

**I/O operations in Windows Store apps:** Mentions differences and considerations when using I/O operations in Windows 8.x Store apps, including alternative namespaces and methods.

**I/O and security:** Emphasizes the need to follow operating system security requirements and access control when using I/O classes, and recommends using isolated storage for .NET applications in certain scenarios.

# How to: Write Text to a File
This article provides examples of different ways to write text to a file in a .NET app. The article covers the usage of various classes and methods for writing text to a file.

## StreamWriter Class
The StreamWriter class provides methods for synchronously or asynchronously writing text to a file. The following examples demonstrate its usage:

### Example: Synchronously write text with StreamWriter

```
class Program
{
    static void Main(string[] args)
    {
        string[] lines = { "First line", "Second line", "Third line" };
        string docPath = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);

        using (StreamWriter outputFile = new StreamWriter(Path.Combine(docPath, "WriteLines.txt")))
        {
            foreach (string line in lines)
                outputFile.WriteLine(line);
        }
    }
}

```
This example writes the contents of the lines array to a file named "WriteLines.txt" synchronously.

### Example: Synchronously append text with StreamWriter

```
class Program
{
    static void Main(string[] args)
    {
        string docPath = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);

        using (StreamWriter outputFile = new StreamWriter(Path.Combine(docPath, "WriteLines.txt"), true))
        {
            outputFile.WriteLine("Fourth Line");
        }
    }
}

```
This example appends the text "Fourth Line" to the file "WriteLines.txt" synchronously.

### Example: Asynchronously write text with StreamWriter
```
class Program
{
    static async Task Main()
    {
        string docPath = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);

        using (StreamWriter outputFile = new StreamWriter(Path.Combine(docPath, "WriteTextAsync.txt")))
        {
            await outputFile.WriteAsync("This is a sentence.");
        }
    }
}

```

This example asynchronously writes the text "This is a sentence." to a file named "WriteTextAsync.txt" using the WriteAsync method.

## File Class
The File class provides static methods for writing text to a file or appending text to an existing file. The following example demonstrates its usage:

### Example: Write and append text with the File class
```
class Program
{
    static void Main(string[] args)
    {
        string text = "First line" + Environment.NewLine;
        string docPath = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments);

        File.WriteAllText(Path.Combine(docPath, "WriteFile.txt"), text);

        string[] lines = { "New line 1", "New line 2" };
        File.AppendAllLines(Path.Combine(docPath, "WriteFile.txt"), lines);
    }
}

```
This example writes the text "First line" to a file named "WriteFile.txt" using WriteAllText, and then appends the lines "New line 1" and "New line 2" to the same file using AppendAllLines.

