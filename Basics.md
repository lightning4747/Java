# Java Basics - Complete Study Guide

## Table of Contents
1. [Introduction to Java](#1-introduction-to-java)
2. [Setting Up Java](#2-setting-up-java)
3. [Basic Syntax](#3-basic-syntax)
4. [Data Types](#4-data-types)
5. [Variables](#5-variables)
6. [Operators](#6-operators)
7. [Control Flow](#7-control-flow)
8. [Arrays](#8-arrays)
9. [Methods](#9-methods)
10. [Object-Oriented Programming](#10-object-oriented-programming)
11. [Exception Handling](#11-exception-handling)
12. [File I/O Basics](#12-file-io-basics)
13. [Study Tips and Next Steps](#study-tips-and-next-steps)

---

## 1. Introduction to Java

Java is a powerful, versatile programming language that has dominated enterprise development and is essential for building robust applications.

### 🌟 What is Java?
- **High-level programming language:** Easy to read and write
- **Object-oriented:** Everything revolves around objects and classes
- **Platform independent:** "Write Once, Run Anywhere" (WORA)
- **Strongly typed:** Variables must be declared with specific types

### 🎯 Key Features

| Feature | Description | Benefit |
|---------|-------------|---------|
| **Simple** | Easy to learn syntax, similar to C++ but cleaner | Faster development |
| **Secure** | Built-in security features, no pointers | Safer applications |
| **Portable** | Runs on any platform with JVM | Cross-platform compatibility |
| **Robust** | Strong memory management, exception handling | Reliable applications |
| **Multithreaded** | Built-in support for concurrent programming | Better performance |

### 🔧 Why Learn Java?
- **Industry standard:** Used by major companies (Google, Amazon, Netflix)
- **Versatile:** Web development, mobile apps (Android), enterprise software
- **Large community:** Extensive libraries and frameworks
- **Career opportunities:** High demand in job market

---

## 2. Setting Up Java

### 📦 Installation Steps

#### Step 1: Install JDK (Java Development Kit)
```bash
# Download from Oracle or OpenJDK
# Windows: Download .exe installer
# macOS: Download .dmg installer  
# Linux: sudo apt install openjdk-11-jdk
```

#### Step 2: Set Environment Variables
```bash
# Windows
JAVA_HOME = C:\Program Files\Java\jdk-11
PATH = %JAVA_HOME%\bin

# macOS/Linux  
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk
export PATH=$JAVA_HOME/bin:$PATH
```

#### Step 3: Verify Installation
```bash
# Check Java version
java -version

# Check compiler version
javac -version

# Expected output: java version "11.0.x"
```

### 🛠️ Development Tools
- **Text Editors:** VS Code, Sublime Text, Atom
- **IDEs:** IntelliJ IDEA, Eclipse, NetBeans
- **Online Editors:** Replit, CodePen, JDoodle

---

## 3. Basic Syntax

### 📝 Your First Java Program

```java
// HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
        System.out.println("Welcome to Java!");
    }
}
```

### 🔍 Code Breakdown

| Component | Purpose | Example |
|-----------|---------|---------|
| `public class HelloWorld` | Class declaration (must match filename) | `HelloWorld.java` |
| `public static void main(String[] args)` | Main method (program entry point) | Required in every program |
| `System.out.println()` | Print text to console | Output method |
| `{}` | Code blocks | Group related statements |
| `//` | Single-line comment | Documentation |
| `/* */` | Multi-line comment | Longer explanations |

### 📋 Java Syntax Rules
- **Case sensitive:** `Main` ≠ `main`
- **Class names:** Must start with uppercase letter (PascalCase)
- **Method names:** Start with lowercase letter (camelCase)
- **File name:** Must match the public class name
- **Semicolons:** End every statement with `;`
- **Braces:** Use `{}` for code blocks

### 💻 Compiling and Running

```bash
# Compile Java source code
javac HelloWorld.java

# Run the compiled program
java HelloWorld

# Output: Hello, World!
```

---

## 4. Data Types

Java has two categories of data types: **primitive** and **reference** types.

### 🔢 Primitive Data Types

#### Integer Types
```java
byte smallNumber = 127;        // 8-bit: -128 to 127
short mediumNumber = 32767;    // 16-bit: -32,768 to 32,767  
int regularNumber = 2147483647; // 32-bit: -2^31 to 2^31-1
long bigNumber = 9223372036854775807L; // 64-bit: -2^63 to 2^63-1
```

#### Floating-Point Types
```java
float price = 19.99f;          // 32-bit: ~7 decimal digits
double precisePrice = 19.99;   // 64-bit: ~15 decimal digits (default)
```

#### Other Primitive Types
```java
boolean isJavaFun = true;      // true or false only
char grade = 'A';              // Single 16-bit Unicode character
char unicodeChar = '\u0041';   // Unicode representation ('A')
```

### 📚 Primitive Types Summary

| Type | Size | Range | Default | Example |
|------|------|-------|---------|---------|
| `byte` | 8-bit | -128 to 127 | 0 | `byte b = 100;` |
| `short` | 16-bit | -32,768 to 32,767 | 0 | `short s = 1000;` |
| `int` | 32-bit | -2³¹ to 2³¹-1 | 0 | `int i = 50000;` |
| `long` | 64-bit | -2⁶³ to 2⁶³-1 | 0L | `long l = 50000L;` |
| `float` | 32-bit | ~7 digits | 0.0f | `float f = 3.14f;` |
| `double` | 64-bit | ~15 digits | 0.0 | `double d = 3.14;` |
| `boolean` | 1-bit | true/false | false | `boolean b = true;` |
| `char` | 16-bit | 0 to 65,535 | '\u0000' | `char c = 'A';` |

### 🏷️ Reference Data Types

```java
// String (most common reference type)
String name = "John Doe";
String message = new String("Hello");

// Arrays
int[] numbers = {1, 2, 3, 4, 5};
String[] names = {"Alice", "Bob", "Charlie"};

// Objects
Scanner scanner = new Scanner(System.in);
ArrayList<String> list = new ArrayList<>();
```

### 🔄 Type Conversion

#### Automatic (Implicit) Conversion
```java
int intValue = 10;
double doubleValue = intValue;  // int to double (widening)
System.out.println(doubleValue); // 10.0
```

#### Manual (Explicit) Conversion
```java
double doubleValue = 10.99;
int intValue = (int) doubleValue;  // double to int (narrowing)
System.out.println(intValue);      // 10 (loses decimal part)
```

---

## 5. Variables

Variables are containers that store data values during program execution.

### 📝 Variable Declaration and Initialization

```java
// Declaration only
int age;
String name;
boolean isStudent;

// Declaration with initialization
int age = 25;
String name = "Alice";
boolean isStudent = true;

// Multiple variables of same type
int x = 5, y = 10, z = 15;

// Constants (cannot be changed)
final double PI = 3.14159;
final String COMPANY_NAME = "TechCorp";
```

### 🏷️ Variable Naming Conventions

#### ✅ Good Practice
```java
int studentAge = 20;           // camelCase
String firstName = "John";     // descriptive names
boolean isValidEmail = true;   // boolean starts with 'is', 'has', 'can'
final int MAX_SIZE = 100;      // constants in UPPER_CASE
```

#### ❌ Avoid
```java
int a = 20;                    // not descriptive
String First_Name = "John";    // don't use underscores
boolean flag = true;           // vague naming
int 2ndValue = 10;            // can't start with number
```

### 📋 Variable Naming Rules
- **Must start with:** letter, underscore `_`, or dollar sign `$`
- **Can contain:** letters, digits, underscores, dollar signs
- **Cannot be:** Java reserved words (`int`, `class`, `public`, etc.)
- **Case sensitive:** `name` ≠ `Name`

### 🔧 Variable Scope

```java
public class ScopeExample {
    static int globalVariable = 100;  // Class scope
    
    public static void main(String[] args) {
        int localVariable = 50;       // Method scope
        
        if (localVariable > 0) {
            int blockVariable = 25;   // Block scope
            System.out.println(blockVariable); // ✅ Valid
        }
        
        // System.out.println(blockVariable); // ❌ Error: out of scope
        System.out.println(localVariable);    // ✅ Valid
        System.out.println(globalVariable);   // ✅ Valid
    }
}
```

---

## 6. Operators

Operators perform operations on variables and values.

### ➕ Arithmetic Operators

```java
int a = 10, b = 3;

// Basic arithmetic
int sum = a + b;        // 13 - Addition
int difference = a - b; // 7  - Subtraction  
int product = a * b;    // 30 - Multiplication
int quotient = a / b;   // 3  - Division (integer division)
int remainder = a % b;  // 1  - Modulus (remainder)

// Increment/Decrement
int x = 5;
x++;        // Post-increment: x becomes 6
++x;        // Pre-increment: x becomes 7
x--;        // Post-decrement: x becomes 6
--x;        // Pre-decrement: x becomes 5
```

### 📊 Assignment Operators

```java
int num = 10;

num += 5;   // num = num + 5;  → 15
num -= 3;   // num = num - 3;  → 12
num *= 2;   // num = num * 2;  → 24
num /= 4;   // num = num / 4;  → 6
num %= 3;   // num = num % 3;  → 0
```

### 🔍 Comparison Operators

```java
int a = 10, b = 5;

boolean result1 = a == b;  // false - Equal to
boolean result2 = a != b;  // true  - Not equal to
boolean result3 = a > b;   // true  - Greater than
boolean result4 = a < b;   // false - Less than
boolean result5 = a >= b;  // true  - Greater than or equal
boolean result6 = a <= b;  // false - Less than or equal
```

### 🧠 Logical Operators

```java
boolean x = true, y = false;

boolean and = x && y;    // false - Logical AND
boolean or = x || y;     // true  - Logical OR  
boolean notX = !x;       // false - Logical NOT

// Short-circuit evaluation
boolean result = (5 > 3) && (10 < 20);  // true (both conditions checked)
boolean result2 = (5 < 3) && (10 < 20); // false (second condition not evaluated)
```

### 🔢 Bitwise Operators (Advanced)

```java
int a = 5;   // 101 in binary
int b = 3;   // 011 in binary

int bitwiseAnd = a & b;   // 001 → 1
int bitwiseOr = a | b;    // 111 → 7
int bitwiseXor = a ^ b;   // 110 → 6
int bitwiseNot = ~a;      // ...11111010 → -6
int leftShift = a << 1;   // 1010 → 10
int rightShift = a >> 1;  // 010 → 2
```

### 🎯 Operator Precedence (High to Low)

1. **Postfix:** `expr++`, `expr--`
2. **Unary:** `++expr`, `--expr`, `+expr`, `-expr`, `~`, `!`
3. **Multiplicative:** `*`, `/`, `%`
4. **Additive:** `+`, `-`
5. **Relational:** `<`, `>`, `<=`, `>=`
6. **Equality:** `==`, `!=`
7. **Logical AND:** `&&`
8. **Logical OR:** `||`
9. **Assignment:** `=`, `+=`, `-=`, etc.

---

## 7. Control Flow

Control flow statements determine the order in which code executes.

### 🔀 If-Else Statements

#### Basic If-Else
```java
int age = 18;

if (age >= 18) {
    System.out.println("You are an adult");
} else {
    System.out.println("You are a minor");
}
```

#### Multiple Conditions
```java
int score = 85;

if (score >= 90) {
    System.out.println("Grade: A");
} else if (score >= 80) {
    System.out.println("Grade: B");
} else if (score >= 70) {
    System.out.println("Grade: C");  
} else if (score >= 60) {
    System.out.println("Grade: D");
} else {
    System.out.println("Grade: F");
}
```

#### Nested If Statements
```java
int age = 25;
boolean hasLicense = true;

if (age >= 18) {
    if (hasLicense) {
        System.out.println("You can drive!");
    } else {
        System.out.println("You need a license to drive");
    }
} else {
    System.out.println("You're too young to drive");
}
```

### 🔄 Switch Statements

```java
String day = "Monday";

switch (day) {
    case "Monday":
        System.out.println("Start of the work week!");
        break;
    case "Tuesday":
    case "Wednesday": 
    case "Thursday":
        System.out.println("Midweek grind!");
        break;
    case "Friday":
        System.out.println("TGIF!");
        break;
    case "Saturday":
    case "Sunday":
        System.out.println("Weekend!");
        break;
    default:
        System.out.println("Invalid day");
        break;
}
```

#### Switch with Numbers
```java
int month = 3;

switch (month) {
    case 12:
    case 1:
    case 2:
        System.out.println("Winter");
        break;
    case 3:
    case 4:
    case 5:
        System.out.println("Spring");
        break;
    case 6:
    case 7:
    case 8:
        System.out.println("Summer");
        break;
    case 9:
    case 10:
    case 11:
        System.out.println("Fall");
        break;
    default:
        System.out.println("Invalid month");
}
```

### 🔁 Loops

#### For Loop
```java
// Basic for loop
for (int i = 0; i < 10; i++) {
    System.out.println("Count: " + i);
}

// Counting backwards
for (int i = 10; i >= 1; i--) {
    System.out.println("Countdown: " + i);
}

// Skip even numbers
for (int i = 1; i < 20; i += 2) {
    System.out.println("Odd number: " + i);
}
```

#### Enhanced For Loop (For-Each)
```java
int[] numbers = {1, 2, 3, 4, 5};

// Enhanced for loop
for (int number : numbers) {
    System.out.println("Number: " + number);
}

String[] names = {"Alice", "Bob", "Charlie"};
for (String name : names) {
    System.out.println("Hello, " + name);
}
```

#### While Loop
```java
int count = 0;

while (count < 5) {
    System.out.println("Count: " + count);
    count++;  // Important: increment to avoid infinite loop
}

// Practical example: input validation
Scanner scanner = new Scanner(System.in);
int number = -1;

while (number < 0) {
    System.out.print("Enter a positive number: ");
    number = scanner.nextInt();
}
```

#### Do-While Loop
```java
int number;
Scanner scanner = new Scanner(System.in);

do {
    System.out.print("Enter a number (0 to exit): ");
    number = scanner.nextInt();
    System.out.println("You entered: " + number);
} while (number != 0);
```

### 🎛️ Loop Control Statements

```java
// Break: exit loop immediately
for (int i = 1; i <= 10; i++) {
    if (i == 5) {
        break;  // Exit loop when i equals 5
    }
    System.out.println(i); // Prints: 1, 2, 3, 4
}

// Continue: skip current iteration
for (int i = 1; i <= 5; i++) {
    if (i == 3) {
        continue;  // Skip when i equals 3
    }
    System.out.println(i); // Prints: 1, 2, 4, 5
}
```

---

## 8. Arrays

Arrays store multiple values of the same type in a single variable.

### 📋 Array Declaration and Initialization

#### Different Ways to Create Arrays
```java
// Method 1: Declaration then initialization
int[] numbers;
numbers = new int[5];  // Creates array of 5 integers

// Method 2: Combined declaration and initialization
int[] numbers = new int[5];

// Method 3: Initialize with values
int[] numbers = {1, 2, 3, 4, 5};

// Method 4: Using new with values
int[] numbers = new int[]{1, 2, 3, 4, 5};

// Different syntax (less common)
int numbers[] = new int[5];  // Valid but not preferred
```

### 🔢 Working with Arrays

#### Accessing and Modifying Elements
```java
int[] scores = {85, 92, 78, 96, 87};

// Accessing elements (zero-based indexing)
int firstScore = scores[0];    // 85
int lastScore = scores[4];     // 87
int thirdScore = scores[2];    // 78

// Modifying elements
scores[1] = 95;  // Changes 92 to 95
scores[0] = 90;  // Changes 85 to 90

// Array length
int arraySize = scores.length; // 5 (property, not method)
```

#### Array Bounds and Safety
```java
int[] numbers = {10, 20, 30};

// Valid access
System.out.println(numbers[0]);  // 10
System.out.println(numbers[2]);  // 30

// Invalid access (throws ArrayIndexOutOfBoundsException)
// System.out.println(numbers[3]);  // ❌ Error!
// System.out.println(numbers[-1]); // ❌ Error!

// Safe access with bounds checking
int index = 3;
if (index >= 0 && index < numbers.length) {
    System.out.println(numbers[index]);
} else {
    System.out.println("Index out of bounds");
}
```

### 🔄 Looping Through Arrays

```java
int[] numbers = {10, 20, 30, 40, 50};

// Traditional for loop
for (int i = 0; i < numbers.length; i++) {
    System.out.println("Index " + i + ": " + numbers[i]);
}

// Enhanced for loop (recommended for simple iteration)
for (int number : numbers) {
    System.out.println("Value: " + number);
}

// While loop
int index = 0;
while (index < numbers.length) {
    System.out.println(numbers[index]);
    index++;
}
```

### 🧮 Common Array Operations

```java
int[] numbers = {5, 2, 8, 1, 9};

// Find maximum value
int max = numbers[0];
for (int i = 1; i < numbers.length; i++) {
    if (numbers[i] > max) {
        max = numbers[i];
    }
}
System.out.println("Maximum: " + max); // 9

// Find minimum value  
int min = numbers[0];
for (int number : numbers) {
    if (number < min) {
        min = number;
    }
}
System.out.println("Minimum: " + min); // 1

// Calculate sum and average
int sum = 0;
for (int number : numbers) {
    sum += number;
}
double average = (double) sum / numbers.length;
System.out.println("Sum: " + sum);           // 25
System.out.println("Average: " + average);   // 5.0
```

### 🔍 Array Searching

```java
String[] names = {"Alice", "Bob", "Charlie", "Diana"};

// Linear search
String searchName = "Charlie";
boolean found = false;
int position = -1;

for (int i = 0; i < names.length; i++) {
    if (names[i].equals(searchName)) {
        found = true;
        position = i;
        break;
    }
}

if (found) {
    System.out.println(searchName + " found at index " + position);
} else {
    System.out.println(searchName + " not found");
}
```

### 📊 Multidimensional Arrays

```java
// 2D Array (matrix)
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

// Accessing 2D array elements
int value = matrix[1][2]; // Second row, third column → 6

// Looping through 2D array
for (int row = 0; row < matrix.length; row++) {
    for (int col = 0; col < matrix[row].length; col++) {
        System.out.print(matrix[row][col] + " ");
    }
    System.out.println(); // New line after each row
}

// Enhanced for loop with 2D arrays
for (int[] row : matrix) {
    for (int value : row) {
        System.out.print(value + " ");
    }
    System.out.println();
}
```

---

## 9. Methods

Methods are reusable blocks of code that perform specific tasks, making programs more modular and organized.

### 📝 Method Structure

```java
// Method syntax
accessModifier static returnType methodName(parameterType parameterName) {
    // Method body
    return value; // if returnType is not void
}
```

### 🔧 Basic Method Examples

#### Methods with No Parameters
```java
public class MathUtils {
    // Method with no parameters, returns value
    public static double getPi() {
        return 3.14159;
    }
    
    // Method with no parameters, no return value
    public static void printGreeting() {
        System.out.println("Hello, welcome to Java!");
    }
    
    public static void main(String[] args) {
        // Calling methods
        double piValue = getPi();
        System.out.println("Pi is: " + piValue);
        
        printGreeting();
    }
}
```

#### Methods with Parameters
```java
public class Calculator {
    // Method with parameters and return value
    public static int add(int a, int b) {
        return a + b;
    }
    
    // Method with multiple parameters
    public static double calculateArea(double length, double width) {
        return length * width;
    }
    
    // Method with different parameter types
    public static void displayPersonInfo(String name, int age, boolean isStudent) {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Student: " + (isStudent ? "Yes" : "No"));
    }
    
    public static void main(String[] args) {
        // Calling methods with arguments
        int sum = add(5, 3);
        System.out.println("Sum: " + sum);
        
        double area = calculateArea(10.5, 8.2);
        System.out.println("Area: " + area);
        
        displayPersonInfo("Alice", 20, true);
    }
}
```

### 🔄 Method Overloading

```java
public class MathOperations {
    // Same method name, different parameters
    
    public static int add(int a, int b) {
        return a + b;
    }
    
    public static double add(double a, double b) {
        return a + b;
    }
    
    public static int add(int a, int b, int c) {
        return a + b + c;
    }
    
    public static String add(String a, String b) {
        return a + b;
    }
    
    public static void main(String[] args) {
        System.out.println(add(5, 3));           // Calls int version
        System.out.println(add(5.5, 3.2));      // Calls double version  
        System.out.println(add(1, 2, 3));       // Calls three-parameter version
        System.out.println(add("Hello", "World")); // Calls String version
    }
}
```

### 📤 Return Types and Void Methods

```java
public class ReturnExamples {
    // Method returning int
    public static int getRandomNumber() {
        return (int)(Math.random() * 100);
    }
    
    // Method returning String
    public static String getFullName(String firstName, String lastName) {
        return firstName + " " + lastName;
    }
    
    // Method returning boolean
    public static boolean isEven(int number) {
        return number % 2 == 0;
    }
    
    // Void method (no return value)
    public static void printTable(int number) {
        for (int i = 1; i <= 10; i++) {
            System.out.println(number + " x " + i + " = " + (number * i));
        }
    }
    
    // Method with early return
    public static String checkAge(int age) {
        if (age < 0) {
            return "Invalid age";
        }
        if (age < 18) {
            return "Minor";
        }
        if (age < 65) {
            return "Adult";
        }
        return "Senior";
    }
}
```

### 🔢 Working with Arrays in Methods

```java
public class ArrayMethods {
    // Method that takes array as parameter
    public static void printArray(int[] array) {
        for (int value : array) {
            System.out.print(value + " ");
        }
        System.out.println();
    }
    
    // Method that returns array
    public static int[] createSequence(int start, int length) {
        int[] sequence = new int[length];
        for (int i = 0; i < length; i++) {
            sequence[i] = start + i;
        }
        return sequence;
    }
    
    // Method that modifies array
    public static void doubleValues(int[] array) {
        for (int i = 0; i < array.length; i++) {
            array[i] *= 2;  // Arrays are passed by reference
        }
    }
    
    // Method that finds maximum in array
    public static int findMax(int[] array) {
        if (array.length == 0) {
            return Integer.MIN_VALUE; // Handle empty array
        }
        
        int max = array[0];
        for (int i = 1; i < array.length; i++) {
            if (array[i] > max) {
                max = array[i];
            }
        }
        return max;
    }
    
    public static void main(String[] args) {
        int[] numbers = {3, 1, 4, 1, 5, 9};
        
        printArray(numbers);                    // 3 1 4 1 5 9
        
        int[] sequence = createSequence(10, 5);
        printArray(sequence);                   // 10 11 12 13 14
        
        doubleValues(numbers);
        printArray(numbers);                    // 6 2 8 2 10 18
        
        int max = findMax(numbers);
        System.out.println("Maximum: " + max); // 18
    }
}
```

### ♻️ Recursive Methods

```java
public class RecursionExamples {
    // Factorial calculation
    public static long factorial(int n) {
        // Base case
        if (n <= 1) {
            return 1;
        }
        // Recursive case
        return n * factorial(n - 1);
    }
    
    // Fibonacci sequence
    public static int fibonacci(int n) {
        if (n <= 1) {
            return n;
        }
        return fibonacci(n - 1) + fibonacci(n - 2);
    }
    
    // Power calculation
    public static double power(double base, int exponent) {
        if (exponent == 0) {
            return 1;
        }
        if (exponent < 0) {
            return 1 / power(base, -exponent);
        }
        return base * power(base, exponent - 1);
    }
    
    public static void main(String[] args) {
        System.out.println("5! = " + factorial(5));        // 120
        System.out.println("Fibonacci(10) = " + fibonacci(10)); // 55
        System.out.println("2^10 = " + power(2, 10));      // 1024.0
    }
}
```
