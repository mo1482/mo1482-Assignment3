# Part G 

## 1. .csproj Contents

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>net8.0</TargetFramework>
    <ImplicitUsings>enable</ImplicitUsings>
    <Nullable>enable</Nullable>
  </PropertyGroup>

</Project>
```

### Confirmation

* `OutputType` is present and set to `Exe`.
* `TargetFramework` is present and set to `net8.0`.
* `ImplicitUsings` is present and set to `enable`.
* `Nullable` is present and set to `enable`.

These four properties are used to configure how the C# project is built and compiled.

---

## 2. Do #region / #endregion change the compiled output?

No. `#region` and `#endregion` do **not** change the compiled output or the program's behavior.

They are only used to organize and group sections of source code. They can make a large file easier to navigate and understand, especially when there are many methods or classes.

Example:

```csharp
#region Helper Methods

static void PrintMessage()
{
    Console.WriteLine("Hello");
}

#endregion
```

The `#region` and `#endregion` directives are removed during preprocessing and do not affect the generated program.

---

## 3. When would you reach for /// XML doc comments instead of a plain //?

I would use `///` XML documentation comments when documenting public classes, methods, properties, or other members that other developers may use.

XML documentation can describe what a method does, its parameters, its return value, and possible exceptions. IDEs such as Visual Studio can use this information to display helpful tooltips and can also generate XML documentation files.

Example:

```csharp
/// <summary>
/// Adds two numbers together.
/// </summary>
/// <param name="a">The first number.</param>
/// <param name="b">The second number.</param>
/// <returns>The sum of the two numbers.</returns>
static int Add(int a, int b)
{
    return a + b;
}
```

A normal `//` comment is better for short explanations about the implementation or logic inside the code.

---

## 4. Why does C# have no true global variables, and what's the closest equivalent?

C# does not have traditional global variables because it is designed around types, classes, encapsulation, and controlled access to data. Allowing unrestricted global variables could make programs harder to maintain and could cause unexpected changes from different parts of the program.

The closest equivalent is a `static` field, usually placed inside a class.

Example:

```csharp
class Program
{
    private static int counter = 0;

    static void Increment()
    {
        counter++;
    }

    static void PrintCounter()
    {
        Console.WriteLine(counter);
    }
}
```

Because `counter` is `static`, there is only one copy associated with the class rather than one copy for each object.

Therefore, a `static` field is commonly used when a value needs to be shared across methods without creating an object.
