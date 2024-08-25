
# C++ Basics

## 1. Creating Variables

In C++, variables are created by specifying the data type followed by the variable name. For example:

```cpp
dataType variableName;
variableName = value;
```
```cpp
dataType variableName = value;
```

## 2. Data Types

Some basic data types in C++ are:

- `int`: Integer (e.g., `int num = 10;`)
- `float`: Floating-point number (e.g., `float num = 10.5;`)
- `double`: Double-precision floating-point number (e.g., `double num = 10.5555;`)
- `char`: Character (e.g., `char letter = 'A';`)
- `bool`: Boolean (e.g., `bool isTrue = true;`)
- `char[]`: Array of characters, commonly used for strings (e.g., `char greeting[] = "Hello";`)

Example:

```cpp
int age = 25;          // Integer data type
float salary = 5000.5;  // Float data type
char grade = 'A';       // Character data type
bool isPassed = true;   // Boolean data type
char name[] = "Alice";  // Character array (string) data type
```

## 3. `cout` - Output to the Console

The `cout` object, along with the insertion operator (`<<`), is used to display output in C++.

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, World!" << endl;
    cout << "The value of age is: " << age << endl;
    return 0;
}
```

## 4. `cin` - Taking Input from the User

The `cin` object, along with the extraction operator (`>>`), is used to take input from the user.

```cpp
#include <iostream>
using namespace std;

int main() {
    int age;
    cout << "Enter your age: ";
    cin >> age;
    cout << "Your age is: " << age << endl;
    return 0;
}
```

## 5. Comments

Comments in C++ are used to explain code and are ignored by the compiler.

- Single-line comments start with `//`.
- Multi-line comments are enclosed between `/*` and `*/`.

```cpp
// This is a single-line comment

/* This is a 
   multi-line comment */
```

## 6. Basic Arithmetic Operators

C++ provides basic arithmetic operators like:

- `+` : Addition
- `-` : Subtraction
- `*` : Multiplication
- `/` : Division
- `%` : Modulus (remainder)

Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10, b = 5;
    cout << "Addition: " << (a + b) << endl;
    cout << "Subtraction: " << (a - b) << endl;
    cout << "Multiplication: " << (a * b) << endl;
    cout << "Division: " << (a / b) << endl;
    cout << "Modulus: " << (a % b) << endl;
    return 0;
}
```

## 7. Conditional Statements

### `if` Statement

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = 10;
    if (number > 0) {
        cout << "The number is positive.";
    }
    return 0;
}
```

### `if-else` Statement

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = -5;
    if (number > 0) {
        cout << "The number is positive.";
    } else {
        cout << "The number is negative.";
    }
    return 0;
}
```

### `if-else if` Statement

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = 0;
    if (number > 0) {
        cout << "The number is positive.";
    } else if (number < 0) {
        cout << "The number is negative.";
    } else {
        cout << "The number is zero.";
    }
    return 0;
}
```

### `switch` Statement

```cpp
#include <iostream>
using namespace std;

int main() {
    char grade = 'A';
    switch (grade) {
        case 'A':
            cout << "Excellent!";
            break;
        case 'B':
            cout << "Good!";
            break;
        default:
            cout << "Invalid grade.";
    }
    return 0;
}
```

## 8. Loops

### `for` Loop

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 5; i++) {
        cout << "Iteration " << i << endl;
    }
    return 0;
}
```

### `while` Loop

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;
    while (i < 5) {
        cout << "Iteration " << i << endl;
        i++;
    }
    return 0;
}
```

### `do-while` Loop

```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;
    do {
        cout << "Iteration " << i << endl;
        i++;
    } while (i < 5);
    return 0;
}
```

## 9. Functions

Functions in C++ allow you to encapsulate code that you can call multiple times.

### Function Declaration and Definition

```cpp
#include <iostream>
using namespace std;

int add(int a, int b) {
    return a + b;
}

int main() {
    int sum = add(5, 3);
    cout << "Sum: " << sum << endl;
    return 0;
}
```

### Function with No Return Value (`void`)

```cpp
#include <iostream>
using namespace std;

void greet() {
    cout << "Hello, World!";
}

int main() {
    greet();
    return 0;
}
```

## 10. Arrays

An array is a collection of elements of the same data type.

### Declaration and Initialization

```cpp
#include <iostream>
using namespace std;

int main() {
    int numbers[5] = {10, 20, 30, 40, 50};
    cout << "First element: " << numbers[0] << endl;
    return 0;
}
```

## 11. Pointers

Pointers store the address of a variable.

```cpp
#include <iostream>
using namespace std;

int num = 10;
int* ptr = &num;  // Pointer to the variable 'num'
cout << "Value of num: " << num << endl;
cout << "Address of num: " << ptr << endl;
```

## 12. Character and String (char, char[])

### `char`

The `char` data type is used to store single characters.

```cpp
char letter = 'A';
cout << "Character: " << letter << endl;
```

### `char[]` - Character Array

A character array is often used to store strings of characters.

```cpp
char greeting[] = "Hello, World!";
cout << greeting << endl;
```

## 13. Classes and Objects

Classes are blueprints for creating objects in C++.

### Declaration and Definition of a Class

```cpp
#include <iostream>
using namespace std;

class Car {
public:
    string brand;
    string model;
    int year;
    
    void honk() {
        cout << "Beep beep!";
    }
};

int main() {
    Car myCar;
    myCar.brand = "Toyota";
    myCar.model = "Corolla";
    myCar.year = 2020;
    
    cout << myCar.brand << " " << myCar.model << " " << myCar.year << endl;
    myCar.honk();
    return 0;
}
```
