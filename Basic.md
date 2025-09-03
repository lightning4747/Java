Java Study Guide: From Basics to Practice

Table of Contents

1. Introduction to Java
2. Setting Up Java Environment
3. Basic Syntax and Structure
4. Variables and Data Types
5. Operators
6. Control Flow Statements
7. Methods
8. Arrays
9. Practice Questions
10. Next Steps
11. Useful Resources

---

1. Introduction to Java <a name="introduction"></a>

Java is a high-level, class-based programming language designed to be platform-independent. It follows the "write once, run anywhere" (WORA) principle through the Java Virtual Machine (JVM).

Key Features:

· Platform independent (runs on JVM)
· Object-oriented
· Secure and robust
· Multithreaded support
· Large standard library

2. Setting Up Java Environment <a name="environment-setup"></a>

Installation Steps:

1. Download JDK (Java Development Kit):
   · Visit Oracle JDK or OpenJDK
   · Download the appropriate version for your OS
2. Install JDK:
   · Follow the installation wizard instructions
3. Verify Installation:
   ```bash
   javac -version
   java -version
   ```

Output:

```
javac 17.0.1
java version "17.0.1" 2021-10-19 LTS
```

3. Basic Syntax and Structure <a name="basic-syntax"></a>

A basic Java program structure:

```java
// Class declaration
public class HelloWorld {
    
    // Main method - entry point
    public static void main(String[] args) {
        
        // Print statement
        System.out.println("Hello, World!");
    }
}
```

Key points:

· Java is case-sensitive
· Class names use PascalCase (HelloWorld)
· Method names use camelCase (main)
· File name must match class name (HelloWorld.java)

4. Variables and Data Types <a name="variables-data-types"></a>

Primitive Data Types:

Type Size Description Example
byte 1 byte 8-bit integer byte b = 100;
short 2 bytes 16-bit integer short s = 10000;
int 4 bytes 32-bit integer int i = 100000;
long 8 bytes 64-bit integer long l = 100000L;
float 4 bytes Single-precision float float f = 10.5f;
double 8 bytes Double-precision float double d = 10.5;
char 2 bytes Single character char c = 'A';
boolean 1 bit true/false value boolean b = true;

Variable Examples:

```java
int age = 25;
double salary = 50000.50;
char grade = 'A';
boolean isJavaFun = true;
String name = "John"; // String is a class, not primitive
```

Type Casting:

```java
// Automatic casting (widening)
int myInt = 9;
double myDouble = myInt;

// Manual casting (narrowing)
double myDouble = 9.78;
int myInt = (int) myDouble;  // Result: 9
```

5. Operators <a name="operators"></a>

Arithmetic Operators:

```java
int a = 10, b = 3;
System.out.println(a + b);  // 13
System.out.println(a - b);  // 7
System.out.println(a * b);  // 30
System.out.println(a / b);  // 3
System.out.println(a % b);  // 1
```

Assignment Operators:

```java
int x = 10;
x += 5;  // x = 15
x -= 3;  // x = 12
x *= 2;  // x = 24
x /= 4;  // x = 6
x %= 4;  // x = 2
```

Comparison Operators:

```java
int a = 5, b = 3;
System.out.println(a == b);  // false
System.out.println(a != b);  // true
System.out.println(a > b);   // true
System.out.println(a < b);   // false
```

Logical Operators:

```java
boolean x = true, y = false;
System.out.println(x && y);  // false
System.out.println(x || y);  // true
System.out.println(!x);      // false
```

6. Control Flow Statements <a name="control-flow"></a>

If-Else Statements:

```java
int number = 10;

if (number > 0) {
    System.out.println("Positive");
} else if (number < 0) {
    System.out.println("Negative");
} else {
    System.out.println("Zero");
}
```

Switch Statement:

```java
int day = 3;
String dayName;

switch (day) {
    case 1: dayName = "Monday"; break;
    case 2: dayName = "Tuesday"; break;
    case 3: dayName = "Wednesday"; break;
    default: dayName = "Invalid";
}
System.out.println(dayName);  // Wednesday
```

Loops:

```java
// For loop
for (int i = 1; i <= 5; i++) {
    System.out.println("Count: " + i);
}

// While loop
int i = 1;
while (i <= 5) {
    System.out.println("Count: " + i);
    i++;
}

// Do-while loop
int j = 1;
do {
    System.out.println("Count: " + j);
    j++;
} while (j <= 5);
```

7. Methods <a name="methods"></a>

Methods are reusable blocks of code.

Basic Method:

```java
public static int addNumbers(int a, int b) {
    return a + b;
}

// Usage
int result = addNumbers(5, 3);
System.out.println("Sum: " + result);  // Sum: 8
```

Method Overloading:

```java
public static int add(int a, int b) {
    return a + b;
}

public static int add(int a, int b, int c) {
    return a + b + c;
}

public static double add(double a, double b) {
    return a + b;
}
```

8. Arrays <a name="arrays"></a>

Arrays store multiple values of the same type.

Array Examples:

```java
// Declaration and initialization
int[] numbers = {1, 2, 3, 4, 5};
String[] names = {"Alice", "Bob", "Charlie"};

// Access elements
System.out.println(numbers[0]);  // 1
System.out.println(names[1]);    // Bob

// Array length
System.out.println(numbers.length);  // 5
```

Array Iteration:

```java
// For loop
for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}

// For-each loop
for (int number : numbers) {
    System.out.println(number);
}
```

Multi-dimensional Arrays:

```java
int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};

System.out.println(matrix[1][2]);  // 6
```

9. Practice Questions <a name="practice-questions"></a>

Question 1: Basic Calculator

Write a program that takes two numbers and an operator (+, -, *, /) and performs the operation.

Question 2: Fibonacci Series

Generate the first n numbers in the Fibonacci sequence.

Question 3: Student Grade Calculator

Calculate grade based on marks:

· 90-100: A
· 80-89: B
· 70-79: C
· 60-69: D
· Below 60: F

Question 4: Array Operations

Create a program that:

1. Initializes an array of 10 integers
2. Finds max and min values
3. Calculates average
4. Searches for a specific value

Question 5: Number Pattern

Print the following pattern:

```
1
12
123
1234
12345
```

---

Solutions

Solution 1: Basic Calculator

```java
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter first number: ");
        double num1 = scanner.nextDouble();
        
        System.out.print("Enter operator (+, -, *, /): ");
        char operator = scanner.next().charAt(0);
        
        System.out.print("Enter second number: ");
        double num2 = scanner.nextDouble();
        
        double result;
        
        switch (operator) {
            case '+': result = num1 + num2; break;
            case '-': result = num1 - num2; break;
            case '*': result = num1 * num2; break;
            case '/': 
                if (num2 != 0) {
                    result = num1 / num2;
                } else {
                    System.out.println("Error: Division by zero!");
                    return;
                }
                break;
            default:
                System.out.println("Invalid operator!");
                return;
        }
        
        System.out.println("Result: " + result);
    }
}
```

Solution 2: Fibonacci Series

```java
import java.util.Scanner;

public class Fibonacci {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter number of terms: ");
        int n = scanner.nextInt();
        
        int first = 0, second = 1;
        System.out.print("Fibonacci: " + first + " " + second);
        
        for (int i = 2; i < n; i++) {
            int next = first + second;
            System.out.print(" " + next);
            first = second;
            second = next;
        }
    }
}
```

Solution 3: Student Grade Calculator

```java
import java.util.Scanner;

public class GradeCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter student's marks: ");
        int marks = scanner.nextInt();
        
        char grade;
        
        if (marks >= 90) grade = 'A';
        else if (marks >= 80) grade = 'B';
        else if (marks >= 70) grade = 'C';
        else if (marks >= 60) grade = 'D';
        else grade = 'F';
        
        System.out.println("Grade: " + grade);
    }
}
```

Solution 4: Array Operations

```java
import java.util.Scanner;

public class ArrayOperations {
    public static void main(String[] args) {
        int[] numbers = {12, 45, 67, 23, 54, 89, 76, 34, 65, 91};
        
        int max = numbers[0];
        int min = numbers[0];
        int sum = 0;
        
        for (int num : numbers) {
            if (num > max) max = num;
            if (num < min) min = num;
            sum += num;
        }
        
        double average = (double) sum / numbers.length;
        
        System.out.println("Max: " + max);
        System.out.println("Min: " + min);
        System.out.println("Average: " + average);
        
        // Search
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter number to search: ");
        int search = scanner.nextInt();
        
        boolean found = false;
        for (int i = 0; i < numbers.length; i++) {
            if (numbers[i] == search) {
                System.out.println("Found at index: " + i);
                found = true;
                break;
            }
        }
        
        if (!found) {
            System.out.println("Number not found");
        }
    }
}
```

Solution 5: Number Pattern

```java
public class NumberPattern {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(j);
            }
            System.out.println();
        }
    }
}
```

10. Next Steps <a name="next-steps"></a>

1. Object-Oriented Programming (OOP)
   · Classes and Objects
   · Inheritance
   · Polymorphism
   · Encapsulation
   · Abstraction
2. Exception Handling
   · try-catch blocks
   · Custom exceptions
   · Finally block
3. Java Collections Framework
   · ArrayList, LinkedList
   · HashMap, HashSet
   · Iterators
4. File I/O Operations
   · Reading from files
   · Writing to files
   · File handling exceptions
5. Advanced Topics
   · Multithreading
   · Java Stream API
   · Lambda expressions
   · Java Database Connectivity (JDBC)

11. Useful Resources <a name="useful-resources"></a>

1. Oracle Java Tutorials
2. W3Schools Java Tutorial
3. GeeksforGeeks Java
4. Java Code Geeks
5. Stack Overflow Java
6. MOOC.fi Java Programming
7. JetBrains Academy Java
8. Baeldung Java

Practice Commands:

```bash
# Compile Java program
javac YourProgram.java

# Run Java program
java YourProgram

# Compile and run with package
javac -d . YourProgram.java
java your.package.YourProgram
```

Keep practicing regularly and build small projects to reinforce your learning!
