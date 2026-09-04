# CSharpBasicsAssignment

## Assignment 4 — Console Apps, Types & Memory Model

This project is a C# Console Application created for Assignment 4.

The assignment covers the main topics from Lecture 01, including project structure, variables, data types, casting, value types, reference types, scope, operators, and the basic stack and heap memory model.

---

## Topics Covered

* C# Solution and Project Structure
* `.csproj` configuration
* Top-level statements
* File-scoped namespaces
* Variables and Data Types
* Runtime Types using `GetType()`
* Implicit Conversion
* Explicit Casting
* `Convert.ToInt32()`
* Integer Division
* Boxing and Unboxing
* Parsing with `int.Parse()`
* Safe Parsing with `int.TryParse()`
* `float` to `decimal` conversion
* Value Types and Reference Types
* Struct Copy Semantics
* Class Reference Semantics
* Stack and Heap Memory Model
* Variable Scope
* Compound Assignment Operators
* Bitwise Operators
* XOR Operator
* LeetCode 136 — Single Number

---

## Project Structure

```text
CSharpBasicsAssignment/
│
├── CSharpBasicsAssignment.csproj
├── Program.cs
├── Order.cs
├── STACK_HEAP.md
├── README.md
└── ANSWERS.md
```

---

## Parts

### Part A — Project & Structure

Explains the role of:

* `.csproj`
* `Program.cs`
* `obj/`
* `bin/`

It also demonstrates the use of a file-scoped namespace and top-level statements.

---

### Part B — Variables, Types & Casting

Demonstrates:

* `int`
* `long`
* `double`
* `decimal`
* `bool`
* `char`
* `string`
* `var`

It also demonstrates implicit conversion, explicit casting, integer division, boxing/unboxing, parsing, and `float` to `decimal` conversion.

---

### Part C — Value vs. Reference Types

The project demonstrates the difference between value types and reference types using:

* `Point` struct
* `Order` class

The `Order` class contains 10 concrete-typed fields and 2 methods:

* `CalculateTotal()`
* `PrintSummary()`

The assignment demonstrates that copying a struct creates an independent value, while copying a class variable copies the reference to the same object.

---

### Part D — Scope & Operators

This part covers:

#### Scope

* Field scope
* Method scope
* Block scope

#### Compound Assignment

* `+=`
* `-=`
* `*=`
* `/=`
* `%=`

#### Bitwise Operators

* `&` — AND
* `|` — OR
* `^` — XOR

---

### Part E — Stack & Heap

`STACK_HEAP.md` contains diagrams showing how references and objects are represented in the stack and heap.

The diagrams use the following sequence:

```csharp
Order o1 = new Order { OrderId = 1, CustomerName = "Ali" };
Order o2 = o1;
o2.IsPaid = true;
```

---

### Part F — LeetCode 136

The project includes a solution for:

**LeetCode 136 — Single Number**

The solution uses the XOR operator.

Example:

```text
Input:  [4, 1, 2, 1, 2]
Output: 4
```

### Complexity

```text
Time Complexity: O(n)
Space Complexity: O(1)
```

No dictionary, sorting, or additional array is used.

---

## Part G — Short Answers

The answers to the theoretical questions are provided in:

```text
ANSWERS.md
```

---

## How to Run

Make sure you are inside the project directory:

```bash
cd CSharpBasicsAssignment
```

Build the project:

```bash
dotnet build
```

Run the application:

```bash
dotnet run
```

---

## Requirements

* .NET SDK
* C# compiler
* Any code editor such as Visual Studio, Visual Studio Code, or JetBrains Rider

---

## Author

CSharpBasicsAssignment — Assignment 4
