
### **Group A**

#### 1. Differentiate between Object-Oriented Programming (OOP) and Object-Based Programming (OBP). Explain some major features of the C# language.

**Answer**:  
**Object-Oriented Programming (OOP)**:

- Follows the principles of encapsulation, inheritance, polymorphism, and abstraction.
- Supports creating reusable and extensible code.

**Object-Based Programming (OBP)**:

- Focuses on using objects but does not support all OOP principles like inheritance and polymorphism.
- Example: JavaScript is object-based but not purely object-oriented.

**Features of C#**:

- **Type-Safe**: Strongly typed language with compile-time type checking.
- **Cross-Platform**: Runs on Windows, Linux, macOS via .NET Core/.NET 6+.
- **Garbage Collection**: Automatic memory management.
- **Language Interoperability**: Supports multiple languages like VB.NET and F#.
- **Rich Library**: Extensive built-in libraries for rapid development.

---

#### 2. Explain the overview of the Microsoft .NET Framework and its components.

**Answer**:  
**Overview**:  
The .NET Framework is a platform for building and running Windows applications. It provides a runtime environment and a robust library.

**Components**:

1. **CLR (Common Language Runtime)**: Executes code and provides services like garbage collection and exception handling.
2. **BCL (Base Class Library)**: A library of reusable types for common functionalities (e.g., IO, networking).
3. **ASP.NET**: For building web applications and services.
4. **ADO.NET**: For database operations.
5. **WPF (Windows Presentation Foundation)**: For desktop GUI applications.
6. **FCL (Framework Class Library)**: A superset of the BCL that includes advanced utilities.

---

#### 3. What do you mean by property in C# language? How is it different from a method? Compare automatic properties with other types of properties using suitable examples.

**Answer**:  
**Property**:  
A member that provides a flexible mechanism to read, write, or compute the values of a private field.

**Difference from Method**:

- **Property**: Encapsulates a field with `get` and `set` accessors.
- **Method**: Encapsulates a block of code that performs operations.

**Example**:

```csharp
class Student {
    // Automatic property
    public string Name { get; set; }
    
    // Regular property
    private int age;
    public int Age {
        get { return age; }
        set {
            if (value > 0) age = value;
        }
    }
}
```

---

#### 4. Define a constructor. Explain different types of constructors used in C# with examples.

**Answer**:  
A **constructor** is a special method used to initialize objects.

**Types**:

1. **Default Constructor**: No parameters.
2. **Parameterized Constructor**: Accepts arguments.
3. **Copy Constructor**: Copies another object.
4. **Static Constructor**: Initializes static members.

**Example**:

```csharp
class Example {
    public int X { get; set; }

    // Default Constructor
    public Example() { X = 0; }

    // Parameterized Constructor
    public Example(int x) { X = x; }

    // Copy Constructor
    public Example(Example obj) { X = obj.X; }
}
```

---

#### 5. Define inheritance. Write a C# program to demonstrate multilevel and multiple inheritance.

**Answer**:  
**Inheritance** allows a class to acquire the properties of another class.

**Program**:

```csharp
using System;

// Multilevel inheritance
class A {
    public void MethodA() => Console.WriteLine("Class A");
}

class B : A {
    public void MethodB() => Console.WriteLine("Class B");
}

class C : B {
    public void MethodC() => Console.WriteLine("Class C");
}

// Multiple inheritance via interface
interface I1 { void InterfaceMethod(); }
interface I2 { void AnotherMethod(); }

class D : I1, I2 {
    public void InterfaceMethod() => Console.WriteLine("Interface I1");
    public void AnotherMethod() => Console.WriteLine("Interface I2");
}

class Program {
    static void Main() {
        C objC = new C();
        objC.MethodA();
        objC.MethodB();
        objC.MethodC();

        D objD = new D();
        objD.InterfaceMethod();
        objD.AnotherMethod();
    }
}
```
#### 6. What are generics? List different types of generic classes. Explain delegates with examples.

**Answer**:  
**Generics**: Generics allow type parameters in classes, methods, or structures, enabling type safety and reusability.

**Types of Generic Classes**:

1. Generic Class: Uses type parameters (`class MyClass<T>`).
2. Generic Interfaces: Allows generic type definitions in interfaces.
3. Generic Delegates: Supports type-safe method references.

**Delegates**:  
A delegate is a type-safe function pointer, enabling methods to be passed as parameters.

**Example**:

```csharp
using System;

class GenericExample<T> {
    public T Add(T a, T b) {
        return (dynamic)a + (dynamic)b;
    }
}

delegate void PrintDelegate(string message);

class Program {
    static void Main() {
        // Generics Example
        var intExample = new GenericExample<int>();
        Console.WriteLine("Sum: " + intExample.Add(3, 7));

        // Delegate Example
        PrintDelegate printer = Console.WriteLine;
        printer("Hello from Delegate!");
    }
}
```

---

#### 7. What do you mean by lambda expression? Explain different types of lambda expressions used in C# with examples.

**Answer**:  
**Lambda Expression**: A concise way to represent anonymous methods using the `=>` operator.

**Types of Lambda Expressions**:

1. **Expression Lambda**: `x => x * x`
2. **Statement Lambda**: `(x, y) => { return x + y; }`

**Example**:

```csharp
using System;

class Program {
    static void Main() {
        Func<int, int> square = x => x * x;
        Console.WriteLine("Square: " + square(4));

        Action<string> greet = name => Console.WriteLine("Hello " + name);
        greet("Alice");
    }
}
```

---

#### 8. What is managed code? Justify the statement: “The .NET Framework is platform-independent and supports language interoperability.”

**Answer**:  
**Managed Code**: Code executed by the CLR, providing features like garbage collection and security.

**Justification**:

- **Platform Independence**: .NET Core/.NET allows applications to run on multiple platforms.
- **Language Interoperability**: CLR supports multiple languages (e.g., C#, VB.NET, F#).

---

#### 9. What is an optional parameter? Write a C# program using enumerations.

**Answer**:  
**Optional Parameter**: Allows parameters to have default values.

**Program**:

```csharp
using System;

enum Department { HR, IT, Finance }
enum College { Arts, Science, Engineering }

class Program {
    static void Display(Department dept = Department.IT) {
        Console.WriteLine($"Department: {dept}");
    }

    static void Display(College college) {
        Console.WriteLine($"College: {college}");
    }

    static void Main() {
        Display();
        Display(College.Engineering);
    }
}
```

---

#### 10. What is the difference between value types and reference types in C#? Explain boxing and unboxing.

**Answer**:

- **Value Types**: Store data directly (e.g., `int`, `float`).
- **Reference Types**: Store references to data (e.g., `class`, `object`).

**Boxing/Unboxing Example**:

```csharp
using System;

class Program {
    static void Main() {
        int value = 42; // Value type
        object obj = value; // Boxing
        int unboxedValue = (int)obj; // Unboxing
        Console.WriteLine($"Boxed: {obj}, Unboxed: {unboxedValue}");
    }
}
```

---

#### 11. What is an interface? Explain with a suitable program.

**Answer**:  
An interface defines a contract with method signatures but no implementation.

**Program**:

```csharp
using System;

interface IFirst {
    void MethodA();
}

interface ISecond {
    void MethodB();
}

class MultiInherit : IFirst, ISecond {
    public void MethodA() => Console.WriteLine("Interface IFirst");
    public void MethodB() => Console.WriteLine("Interface ISecond");
}

class Program {
    static void Main() {
        MultiInherit obj = new MultiInherit();
        obj.MethodA();
        obj.MethodB();
    }
}
```
## Group B Solutions

### Question 1: Finalizers and `base` Keyword

**What is a Finalizer?**

- A finalizer is a special method in C# used to clean up unmanaged resources before an object is destroyed by the garbage collector.
- It is defined using a tilde (`~`) followed by the class name.

**Example of a Finalizer:**

```csharp
class FinalizerDemo {
    ~FinalizerDemo() {
        Console.WriteLine("Finalizer called");
    }
}
```

**Using the `base` Keyword:**

- The `base` keyword is used to call a member or constructor of the parent class from a derived class.

**Example:**

```csharp
class Parent {
    public Parent() {
        Console.WriteLine("Parent Constructor");
    }
    public void DisplayParent() {
        Console.WriteLine("Parent Method");
    }
}

class Child : Parent {
    public Child() : base() {
        Console.WriteLine("Child Constructor");
    }
    public void DisplayChild() {
        base.DisplayParent();
    }
}

class Program {
    static void Main() {
        Child child = new Child();
        child.DisplayChild();
    }
}
```

---

### Question 2: Exception Handling

**Keywords Used in Exception Handling:**

- `try`: Defines a block of code to monitor for exceptions.
- `catch`: Defines a block of code to handle specific exceptions.
- `finally`: Defines a block of code to execute regardless of whether an exception is thrown.
- `throw`: Used to explicitly throw an exception.

**Program to Handle Exceptions:**

```csharp
class ExceptionHandlingDemo {
    public static void HandleExceptions() {
        try {
            int[] numbers = { 1, 2, 3 };
            Console.WriteLine(numbers[5]); // IndexOutOfRangeException

            object str = "string";
            int num = (int)str; // InvalidCastException
        } catch (IndexOutOfRangeException ex) {
            Console.WriteLine("IndexOutOfRangeException: " + ex.Message);
        } catch (InvalidCastException ex) {
            Console.WriteLine("InvalidCastException: " + ex.Message);
        } finally {
            Console.WriteLine("Final block executed.");
        }
    }

    static void Main() {
        HandleExceptions();
    }
}
```

---

### Question 3: LINQ Query Syntax

**What is Query Syntax in LINQ?**

- LINQ (Language Integrated Query) allows querying of data using SQL-like syntax in C#.
- Query syntax is declarative and uses keywords like `from`, `where`, and `select`.

**Standard Query Operators in LINQ:**

- `select`: Specifies the data to retrieve.
- `contains`: Checks if a collection contains a specific element.
- `orderBy`: Sorts the data in ascending order.
- `where`: Filters the data based on a condition.

**Example Program:**

```csharp
class LINQDemo {
    public static void ShowLINQQueries() {
        List<int> numbers = new List<int> { 1, 2, 3, 4, 5, 6 };

        // Select even numbers
        var evenNumbers = from num in numbers
                          where num % 2 == 0
                          select num;

        Console.WriteLine("Even Numbers: " + string.Join(", ", evenNumbers));

        // Check if the collection contains the number 3
        var containsThree = numbers.Contains(3);
        Console.WriteLine("Contains 3: " + containsThree);

        // Order numbers in descending order
        var descendingNumbers = from num in numbers
                                orderby num descending
                                select num;

        Console.WriteLine("Descending Order: " + string.Join(", ", descendingNumbers));
    }

    static void Main() {
        ShowLINQQueries();
    }
}
```

---

### Question 4: Virtual Methods

**What are Virtual Methods?**

- Virtual methods allow derived classes to override the functionality of a method in the base class.
- Use the `virtual` keyword in the base class and the `override` keyword in the derived class.

**Program Example:**

```csharp
class BaseClass {
    public virtual void Display() {
        Console.WriteLine("Base Display");
    }
}

class DerivedClass : BaseClass {
    public override void Display() {
        Console.WriteLine("Derived Display");
    }
}

class Program {
    static void Main() {
        BaseClass obj = new DerivedClass();
        obj.Display();
    }
}
```

---

### Question 5: Operator Overloading

**What is Operator Overloading?**

- Operator overloading allows defining custom behavior for operators when applied to user-defined types.

**Program to Overload a Binary Operator:**

```csharp
class Complex {
    public int Real { get; set; }
    public int Imaginary { get; set; }

    public Complex(int real, int imaginary) {
        Real = real;
        Imaginary = imaginary;
    }

    public static Complex operator +(Complex a, Complex b) {
        return new Complex(a.Real + b.Real, a.Imaginary + b.Imaginary);
    }

    public override string ToString() {
        return $"{Real} + {Imaginary}i";
    }
}

class Program {
    static void Main() {
        Complex c1 = new Complex(1, 2);
        Complex c2 = new Complex(3, 4);
        Complex sum = c1 + c2;
        Console.WriteLine("Sum: " + sum);
    }
}
```

---

### Question 6: Database Insert and Select

**Program to Insert and Select Data:**

```csharp
using System;
using System.Data.SqlClient;

class DatabaseDemo {
    public static void InsertData() {
        string connectionString = "your_connection_string_here";
        string query = "INSERT INTO Students (Name, Age) VALUES ('Alice', 20)";

        using (SqlConnection connection = new SqlConnection(connectionString)) {
            SqlCommand command = new SqlCommand(query, connection);
            connection.Open();
            command.ExecuteNonQuery();
            Console.WriteLine("Data inserted successfully.");
        }
    }

    public static void SelectData() {
        string connectionString = "your_connection_string_here";
        string query = "SELECT * FROM Students";

        using (SqlConnection connection = new SqlConnection(connectionString)) {
            SqlCommand command = new SqlCommand(query, connection);
            connection.Open();
            SqlDataReader reader = command.ExecuteReader();

            while (reader.Read()) {
                Console.WriteLine($"ID: {reader["ID"]}, Name: {reader["Name"]}, Age: {reader["Age"]}");
            }
        }
    }

    static void Main() {
        InsertData();
        SelectData();
    }
}
```

---

### Question 7: ASP.NET Components and Validation Controls

**Components of ASP.NET:**

- **Server Controls:** Used to create web forms.
- **Master Pages:** Provides templates for consistent page layout.
- **State Management:** Maintains data across requests.
- **Caching:** Improves application performance by storing data.

**Validation Server Controls:**

1. **RequiredFieldValidator:** Ensures a field is not empty.
2. **RangeValidator:** Validates if a value is within a specific range.
3. **CompareValidator:** Compares values of two controls.
4. **RegularExpressionValidator:** Validates input against a regular expression.
5. **CustomValidator:** Allows custom validation logic.

**Program Example:**

```html
<asp:TextBox ID="txtAge" runat="server"></asp:TextBox>
<asp:RangeValidator ID="RangeValidator1" runat="server" 
    ControlToValidate="txtAge" MinimumValue="18" MaximumValue="65" 
    ErrorMessage="Age must be between 18 and 65"></asp:RangeValidator>
<asp:Button ID="btnSubmit" runat="server" Text="Submit" />
```

---

## Group C Solutions

### Question 1a: User Registration Form

**Create a User Registration Form in ASP.NET:**

1. **Form Page:**

```html
<asp:TextBox ID="txtName" runat="server"></asp:TextBox>
<asp:TextBox ID="txtEmail" runat="server"></asp:TextBox>
<asp:Button ID="btnSubmit" runat="server" Text="Submit" OnClick="SubmitForm" />
```

2. **Display Page:**

```csharp
protected void SubmitForm(object sender, EventArgs e) {
    string name = txtName.Text;
    string email = txtEmail.Text;
    Response.Redirect($"Display.aspx?name={name}&email={email}");
}
```

### Question 1b: Exception Handling in ASP.NET

```csharp
try {
    // Code that might throw an exception
} catch (Exception ex) {
    Response.Write("Error: " + ex.Message);
}
```

---

### Question 2a: Events in C#

**Event Example:**

```csharp
class EventDemo {
    public event Action<string> OnMessage;

    public void TriggerEvent(string message) {
        OnMessage?.Invoke(message);
    }
}
```

### Question 2b: Lambda Expressions and Generic Delegates

```csharp
Func<int, int, int> add = (x, y) => x + y;
Console.WriteLine("Sum: " + add(5, 10));
```

---

### Question 3a: Using `this` Keyword for Indexer

```csharp
class IndexerExample {
    private string[] names = new string[5];

    public string this[int index] {
        get { return names[index]; }
        set { names[index] = value; }
    }
}
```

### Question 3b: Operator Overloading

```csharp
class OverloadOperators {
    public int Value { get; set; }

    public static OverloadOperators operator ++(OverloadOperators obj) {
        obj.Value++;
        return obj;
    }

    public static bool operator ==(OverloadOperators a, OverloadOperators b) {
        return a.Value == b.Value;
    }
}
```