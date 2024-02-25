# Gemini vs. Copilot vs. ChatGPT 3.5

## 2024-02-25

### Prompt: _Create markdown table that shows the top ten C# best practices with good and bad examples_




### Formatting

Winner: Copilot - it formatted the markdown so that it could be copied and pasted.

Loser: Gemini - looks great on the Gemini screen, but I had to modify the markdown by hand. [maybe I just don't know the write prompt]


### Content
All of the AI made reasonable attempts at best practices.




## copilot 2024.02.25


| **Best Practice** | **Good Example** | **Bad Example** |
|-------------------|------------------|------------------|
| **1. Naming Conventions** | Use **Pascal case** for class names, method names, and constants. Use **Camel case** for method arguments and local variables. | **Bad:** `public void m()`<br>**Good:** `public void CalculateTotalPrice(int quantity)` |
| **2. Meaningful Names** | Choose descriptive names for classes, methods, and properties. | **Bad:** `public class XYZ`<br>**Good:** `public class OrderProcessor` |
| **3. Member Variable Placement** | Declare member variables and fields at the top of the class. | **Bad:** Fields scattered throughout the class. |
| **4. Avoid Magic Numbers** | Use named constants or enums instead of hardcoding values. | **Bad:** `if (status == 2)`<br>**Good:** `if (status == OrderStatus.Processing)` |
| **5. Proper Exception Handling** | Handle exceptions gracefully with try-catch blocks. | **Bad:** Swallowing exceptions without logging or handling. |
| **6. Avoid Global Variables** | Minimize global variables; prefer local scope. | **Bad:** Overusing global variables. |
| **7. Use LINQ Effectively** | Write concise LINQ queries for data manipulation. | **Bad:** Nested loops instead of LINQ. |
| **8. Code Comments** | Add comments to explain complex logic or non-obvious behavior. | **Bad:** No comments or outdated comments. |
| **9. SOLID Principles** | Follow SOLID principles (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion). | **Bad:** Monolithic classes violating SRP. |
| **10. Code Formatting** | Consistently format code (indentation, spacing, etc.). | **Bad:** Inconsistent formatting across files. |

---

## ChatGPT 3.5

[not sure how to prompt it to make it copy/pasteable]
| Best Practice                                      | Good Example                                                                                 | Bad Example                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Use meaningful variable and method names          | ```csharp                                                                                     | ```csharp                                                                                     |
|                                                    | int numberOfStudents;                                                                         | int n;                                                                                        |
|                                                    |                                                                                                |                                                                                              |
|                                                    | void CalculateAreaOfRectangle(int length, int width) { /* Calculation logic */ }           | void Calc(int a, int b) { /* Calculation logic */ }                                         |
|                                                    |                                                                                                |                                                                                              |
| Follow coding conventions                          | ```csharp                                                                                     | ```csharp                                                                                     |
|                                                    | class MyClass                                                                                 | class myClass                                                                                 |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     void MyMethod()                                                                           |     void myMethod()                                                                           |
|                                                    |     { /* Method body */ }                                                                     |     { /* Method body */ }                                                                     |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    |                                                                                                |                                                                                              |
| Use comments for clarity                           | ```csharp                                                                                     | ```csharp                                                                                     |
|                                                    | // Calculate the area of a rectangle                                                         | int Area(int l, int w) { /* Calculation logic */ }                                          |
|                                                    | int CalculateArea(int length, int width) { /* Calculation logic */ }                         |                                                                                              |
|                                                    | {                                                                                              |                                                                                              |
|                                                    |     return length * width;                                                                    |                                                                                              |
|                                                    | }                                                                                              |                                                                                              |
|                                                    |                                                                                                |                                                                                              |
| Always validate input parameters                   | ```csharp                                                                                     | ```csharp                                                                                     |
|                                                    | void Divide(int dividend, int divisor)                                                       | void Divide(int a, int b)                                                                    |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     if (divisor != 0)                                                                         |     {                                                                                          |
|                                                    |     {                                                                                          |         // No validation of divisor                                                           |
|                                                    |         int result = dividend / divisor;                                                      |         int result = a / b;                                                                    |
|                                                    |         Console.WriteLine("Result: " + result);                                              |         Console.WriteLine("Result: " + result);                                              |
|                                                    |     }                                                                                          |     }                                                                                          |
|                                                    |     else                                                                                       |     else                                                                                       |
|                                                    |     {                                                                                          |     {                                                                                          |
|                                                    |         Console.WriteLine("Divisor cannot be zero");                                         |         Console.WriteLine("Result: Undefined");                                               |
|                                                    |     }                                                                                          |     }                                                                                          |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    |                                                                                                |                                                                                              |
| Use exception handling                             | ```csharp                                                                                     | ```csharp                                                                                     |
|                                                    | try                                                                                            | try                                                                                            |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     // Code that may throw an exception                                                       |     // Code that may throw an exception                                                       |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    | catch (Exception ex)                                                                          | catch (Exception e)                                                                            |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     // Handle the exception                                                                   |     // Handle the exception                                                                   |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    |                                                                                                |                                                                                              |
| Use object-oriented principles                     | ```csharp                                                                                     | ```csharp                                                                                     |
|                                                    | public class Animal                                                                           | public class Animal                                                                           |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     public virtual void MakeSound()                                                           |     public void MakeSound()                                                                   |
|                                                    |     {                                                                                          |     {                                                                                          |
|                                                    |         Console.WriteLine("Making a sound");                                                 |         Console.WriteLine("Making a sound");                                                 |
|                                                    |     }                                                                                          |     }                                                                                          |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    |                                                                                                |                                                                                              |
|                                                    | public class Dog : Animal                                                                     | public class Dog : Animal                                                                     |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     public override void MakeSound()                                                          |     public void Bark()                                                                        |
|                                                    |     {                                                                                          |     {                                                                                          |
|                                                    |         Console.WriteLine("Barking");                                                        |         Console.WriteLine("Barking");                                                        |
|                                                    |     }                                                                                          |     }                                                                                          |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    |                                                                                                |                                                                                              |
| Keep methods and classes small and focused          | ```csharp                                                                                     | ```csharp                                                                                     |
|                                                    | class MathHelper                                                                               | class MathHelper                                                                               |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     public int Add(int a, int b)                                                              |     public int Add(int a, int b)                                                              |
|                                                    |     {                                                                                          |     {                                                                                          |
|                                                    |         return a + b;                                                                          |         return a + b + 10;                                                                    |
|                                                    |     }                                                                                          |     }                                                                                          |
|                                                    |                                                                                                |                                                                                              |
|                                                    |     public int Subtract(int a, int b)                                                         |     public int Subtract(int a, int b)                                                         |
|                                                    |     {                                                                                          |     {                                                                                          |
|                                                    |         return a - b;                                                                          |         return a - b;                                                                          |
|                                                    |     }                                                                                          |     }                                                                                          |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    |                                                                                                |                                                                                              |
| Handle exceptions at the appropriate level          | ```csharp                                                                                     | ```csharp                                                                                     |
|                                                    | try                                                                                            | try                                                                                            |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     // Code that may throw an exception                                                       |     // Code that may throw an exception                                                       |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    | catch (ArgumentException ex)                                                                 | catch (ArgumentException ex)                                                                 |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     // Handle ArgumentException                                                              |     // Handle ArgumentException                                                              |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    | catch (Exception ex)                                                                          | catch (Exception ex)                                                                          |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     // Handle other exceptions                                                                |     // Handle all exceptions                                                                 |
|                                                    | }                                                                                              | }                                                                                              |
|                                                    |                                                                                                |                                                                                              |
| Use IDisposable for unmanaged resources             | ```csharp                                                                                     | ```csharp                                                                                     |
|                                                    | public class FileManager : IDisposable                                                        | public class FileManager : IDisposable                                                        |
|                                                    | {                                                                                              | {                                                                                              |
|                                                    |     private FileStream _fileStream;                                                           |     private FileStream _fileStream;                                                           |
|                                                    |                                                                                                |                                                                                              |
|                                                    |     public FileManager(string filePath)                                                      |     public FileManager(string filePath)                                                      |
|                                                    |     {                                                                                          |     {                                                                                          |
|                                                    |         _fileStream = new FileStream(filePath, FileMode.Open);                               |         _fileStream = new FileStream(filePath, FileMode.Open);                               |
|                                                    |     }                                                                                          |     }                                                                                          |
|                                                    |                                                                                                |                                                                                              |
|                                                    |     public void Dispose()                                                                     |     public void CloseFile()                                                                   |
|                                                    |     {                                                                                          |     {                                                                                          |
|                                                    |         _fileStream.Dispose();                                                                |         _fileStream.Close();                                                                  |
|                                                    |     }                                                                                          |     }                                                                                          |
|                                                    | }                                                                                              | }                                                                                              |
---
## Gemini
| Best Practice | Good Example | Bad Example |
|-------------------|------------------|------------------|
| 1. Follow Consistent Naming Conventions | customerName, calculateDiscount, OrderProcessor | custName, calcDisc, OrderProc | 
| 2. Use Meaningful Names | customerAddress, calculateTotalCost, validateUserInput | address, calc, validate |
| 3. Use Proper Code Organization | Separate classes for models, controllers, and views | All logic in a single large class |
| 4. Avoid Magic Numbers and Strings | Use constants for frequently used values: const int MAX_LENGTH = 100; | Use hardcoded values: if (age > 18) ... |
| 5. Use Comments Sparingly and Effectively | Explain complex logic, not obvious code | Comment every line: // Set the name |
| 6. Write Readable and Maintainable Code | Use proper indentation, spacing, and formatting | Unformatted code with nested logic |
| 7. Handle Exceptions Properly | Use try-catch blocks to handle potential errors | Ignore exceptions or use bare catch blocks |
| 8. Avoid Code Duplication | Extract common functionality into reusable methods | Duplicate the same logic in multiple places |
| 9. Write Unit Tests for Your Code | Test individual units of code to ensure correctness | No tests or only manual testing |
| 10. Use LINQ to Simplify Complex Queries | Use LINQ for concise and readable data manipulation | Write complex nested loops for data processing |
