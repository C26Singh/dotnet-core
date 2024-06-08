C# 1.0 (2002)
Key Features:

Basic syntax and object-oriented programming principles.
Example:

csharp
Copy code
public class HelloWorld
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
C# 2.0 (2005)
Key Features:

Generics: Type-safe data structures.
Iterators: Simplify collection traversal using yield.
Partial Classes: Split a class across multiple files.
Nullable Types: Allow value types to be null.
Example:

csharp
Copy code
// Generics
List<int> numbers = new List<int> { 1, 2, 3 };

// Iterators
public IEnumerable<int> GetNumbers()
{
    yield return 1;
    yield return 2;
    yield return 3;
}

// Nullable Types
int? nullableInt = null;
C# 3.0 (2007)
Key Features:

LINQ (Language Integrated Query): Query capabilities integrated into C#.
Lambda Expressions: Shorter syntax for anonymous methods.
Anonymous Types: Define classes without explicitly declaring them.
Automatic Properties: Simplify property declarations.
Example:

csharp
Copy code
// LINQ and Lambda Expressions
var numbers = new List<int> { 1, 2, 3, 4 };
var evenNumbers = numbers.Where(n => n % 2 == 0);

// Anonymous Types
var person = new { Name = "John", Age = 30 };

// Automatic Properties
public string Name { get; set; }
C# 4.0 (2010)
Key Features:

Dynamic Typing: Enables dynamic programming.
Named and Optional Parameters: More flexibility in method calls.
Embedded Interop Types: Simplify COM interop.
Example:

csharp
Copy code
// Dynamic Typing
dynamic expando = new System.Dynamic.ExpandoObject();
expando.Name = "John";

// Named and Optional Parameters
void Print(string message = "Hello", int number = 0) { }
Print(number: 5);
C# 5.0 (2012)
Key Features:

Async and Await: Simplify asynchronous programming.
Caller Info Attributes: Retrieve information about the caller of a method.
Example:

csharp
Copy code
// Async and Await
async Task<int> FetchDataAsync()
{
    await Task.Delay(1000);
    return 42;
}
C# 6.0 (2015)
Key Features:

Auto-Property Initializers: Set default values for properties.
Expression-bodied Members: Concise syntax for methods and properties.
String Interpolation: Embed expressions within string literals.
Null-conditional Operator: Simplify null checks.
Example:

csharp
Copy code
// Auto-Property Initializers
public string Name { get; set; } = "Unknown";

// Expression-bodied Members
public override string ToString() => $"Name: {Name}";

// String Interpolation
var name = "John";
var message = $"Hello, {name}!";

// Null-conditional Operator
string text = null;
int? length = text?.Length;
C# 7.0 - 7.3 (2017-2018)
Key Features:

Tuples and Deconstruction: Simplify returning multiple values.
Pattern Matching: Enhanced switch statements and is expressions.
Local Functions: Define functions within other functions.
Ref Returns and Locals: More control over memory usage.
Example:

csharp
Copy code
// Tuples and Deconstruction
(int, string) GetPerson() => (1, "John");
var (id, name) = GetPerson();

// Pattern Matching
object obj = 1;
if (obj is int number)
{
    Console.WriteLine(number);
}

// Local Functions
void OuterFunction()
{
    void InnerFunction() => Console.WriteLine("Hello from Inner");
    InnerFunction();
}
C# 8.0 (2019)
Key Features:

Nullable Reference Types: Improve null safety by distinguishing between nullable and non-nullable references.
Async Streams: Asynchronous iteration with IAsyncEnumerable<T>.
Default Interface Methods: Add methods to interfaces with implementations.
Ranges and Indices: Simplify array slicing.
Example:

csharp
Copy code
// Nullable Reference Types
string? nullableString = null;
string nonNullableString = "Hello";

// Async Streams
async IAsyncEnumerable<int> GetNumbersAsync()
{
    for (int i = 0; i < 10; i++)
    {
        yield return i;
        await Task.Delay(100);
    }
}

// Ranges and Indices
string[] words = { "Hello", "World" };
var slice = words[1..]; // "World"
C# 9.0 (2020)
Key Features:

Records: Immutable data objects with built-in value equality.
Init-only Setters: Allow properties to be set only during object initialization.
Top-level Statements: Simplify program entry points.
Pattern Matching Enhancements: Improved pattern matching.
Example:

csharp
Copy code
// Records
public record Person(string Name, int Age);

// Init-only Setters
public string Name { get; init; }

// Top-level Statements
Console.WriteLine("Hello, World!");
C# 10.0 (2021)
Key Features:

Global Using Directives: Define using directives globally for the entire project.
File-scoped Namespaces: Reduce indentation for namespaces.
Record Structs: Value type records.
Extended Property Patterns: More expressive property patterns.
Example:

csharp
Copy code
// Global Using Directives
global using System;

// File-scoped Namespaces
namespace MyNamespace;

public class MyClass { }

// Record Structs
public record struct Point(int X, int Y);

// Extended Property Patterns
bool IsDefault(Point point) => point is { X: 0, Y: 0 };
C# 11.0 (2022)
Key Features:

Raw String Literals: Simplify multi-line strings with less escaping.
List Patterns: More powerful pattern matching with lists.
Static Abstract Members in Interfaces: Allow static members in interfaces.
Example:

csharp
Copy code
// Raw String Literals
string json = """
{
    "name": "John",
    "age": 30
}
""";

// List Patterns
bool IsFirstElementZero(int[] numbers) => numbers is [0, ..];

// Static Abstract Members in Interfaces
public interface IParseable<T>
{
    static abstract T Parse(string input);
}
C# 12.0 (2024)
Key Features:

Primary Constructors for Classes: Simplify constructor syntax for classes.
Enhanced Interpolated Strings: Improved string interpolation capabilities.
Default Interface Members Enhancements: More flexibility in interface implementations.
Example:

csharp
Copy code
// Primary Constructors for Classes
public class Person(string name, int age)
{
    public string Name { get; } = name;
    public int Age { get; } = age;
}

// Enhanced Interpolated Strings
var name = "John";
var message = $"Hello, {name.ToUpper()}!";
