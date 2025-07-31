# C Programming Practice Questions and Answers

## Question 1: Write a program to print "Hello, World!"

**Answer:**

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

**Explanation:**
- `#include <stdio.h>` includes the standard input/output library
- `printf()` is a function used to print text to the console
- `\n` is an escape sequence for a new line
- `return 0` indicates successful program execution

---

## Question 2: Program to take input and print integer

**Answer:**

```c
#include <stdio.h>

int main() {
    int number;
    printf("Enter an integer: ");
    scanf("%d", &number);
    printf("You entered: %d\n", number);
    return 0;
}
```

**Explanation:**
- `int number;` declares an integer variable
- `scanf("%d", &number);` reads an integer from user input
- `&number` is the address of the variable where the input will be stored
- `%d` is the format specifier for integers

---

## Question 3: Add two numbers entered by user

**Answer:**

```c
#include <stdio.h>

int main() {
    int num1, num2, sum;
    
    printf("Enter first number: ");
    scanf("%d", &num1);
    
    printf("Enter second number: ");
    scanf("%d", &num2);
    
    sum = num1 + num2;
    printf("Sum = %d\n", sum);
    
    return 0;
}
```

**Explanation:**
- Declares three variables: two for input, one for result
- Uses `scanf()` to get user input for both numbers
- Performs addition using the `+` operator
- Prints the result using `printf()`

---

## Question 4: Find size of int, float, double, and char

**Answer:**

```c
#include <stdio.h>

int main() {
    printf("Size of int: %zu bytes\n", sizeof(int));
    printf("Size of float: %zu bytes\n", sizeof(float));
    printf("Size of double: %zu bytes\n", sizeof(double));
    printf("Size of char: %zu bytes\n", sizeof(char));
    return 0;
}
```

**Explanation:**
- `sizeof()` operator returns the size of a data type in bytes
- `%zu` is the format specifier for `size_t` (return type of sizeof)
- Size varies depending on the compiler and system architecture

---

## Question 5: Swap two numbers using a third variable

**Answer:**

```c
#include <stdio.h>

int main() {
    int a, b, temp;
    
    printf("Enter first number: ");
    scanf("%d", &a);
    printf("Enter second number: ");
    scanf("%d", &b);
    
    printf("Before swapping: a = %d, b = %d\n", a, b);
    
    // Swapping using third variable
    temp = a;
    a = b;
    b = temp;
    
    printf("After swapping: a = %d, b = %d\n", a, b);
    return 0;
}
```

**Explanation:**
- Uses a temporary variable `temp` to store one value
- Step 1: Store `a` in `temp`
- Step 2: Assign `b` to `a`
- Step 3: Assign `temp` (original `a`) to `b`

---

## Question 6: Swap two numbers without using a third variable

**Answer:**

```c
#include <stdio.h>

int main() {
    int a, b;
    
    printf("Enter first number: ");
    scanf("%d", &a);
    printf("Enter second number: ");
    scanf("%d", &b);
    
    printf("Before swapping: a = %d, b = %d\n", a, b);
    
    // Swapping without third variable using arithmetic
    a = a + b;
    b = a - b;
    a = a - b;
    
    printf("After swapping: a = %d, b = %d\n", a, b);
    return 0;
}
```

**Alternative Method (XOR):**
```c
// Using XOR operation
a = a ^ b;
b = a ^ b;
a = a ^ b;
```

**Explanation:**
- Arithmetic method: Uses addition and subtraction
- XOR method: Uses bitwise XOR operation
- Both methods avoid using extra memory

---

## Question 7: Print ASCII value of a character

**Answer:**

```c
#include <stdio.h>

int main() {
    char ch;
    
    printf("Enter a character: ");
    scanf("%c", &ch);
    
    printf("ASCII value of '%c' is %d\n", ch, ch);
    return 0;
}
```

**Explanation:**
- Characters are stored as ASCII values internally
- When we print a character as integer, it shows its ASCII value
- ASCII values range from 0 to 127 for standard characters

---

## Question 8: Multiply two floating point numbers

**Answer:**

```c
#include <stdio.h>

int main() {
    float num1, num2, product;
    
    printf("Enter first number: ");
    scanf("%f", &num1);
    printf("Enter second number: ");
    scanf("%f", &num2);
    
    product = num1 * num2;
    printf("Product = %.2f\n", product);
    
    return 0;
}
```

**Explanation:**
- Uses `float` data type for decimal numbers
- `%f` is the format specifier for float
- `%.2f` prints float with 2 decimal places
- `*` operator performs multiplication

---

## Question 9: Find quotient and remainder

**Answer:**

```c
#include <stdio.h>

int main() {
    int dividend, divisor, quotient, remainder;
    
    printf("Enter dividend: ");
    scanf("%d", &dividend);
    printf("Enter divisor: ");
    scanf("%d", &divisor);
    
    quotient = dividend / divisor;
    remainder = dividend % divisor;
    
    printf("Quotient = %d\n", quotient);
    printf("Remainder = %d\n", remainder);
    
    return 0;
}
```

**Explanation:**
- `/` operator gives quotient (integer division)
- `%` operator gives remainder (modulo)
- Both operands should be integers for proper results

---

## Question 10: Print your name using printf

**Answer:**

```c
#include <stdio.h>

int main() {
    printf("My name is John Doe\n");
    return 0;
}
```

**Explanation:**
- Simply use `printf()` with a string containing your name
- Replace "John Doe" with your actual name

---

## Question 11: Take name input using scanf and display it

**Answer:**

```c
#include <stdio.h>

int main() {
    char name[50];
    
    printf("Enter your name: ");
    scanf("%s", name);
    
    printf("Hello, %s!\n", name);
    return 0;
}
```

**Explanation:**
- `char name[50]` declares a character array (string) of size 50
- `%s` is the format specifier for strings
- Note: `scanf("%s")` stops reading at whitespace

---

## Question 12: Convert kilometers to miles

**Answer:**

```c
#include <stdio.h>

int main() {
    float kilometers, miles;
    
    printf("Enter distance in kilometers: ");
    scanf("%f", &kilometers);
    
    miles = kilometers * 0.621371;
    printf("%.2f kilometers = %.2f miles\n", kilometers, miles);
    
    return 0;
}
```

**Explanation:**
- 1 kilometer = 0.621371 miles
- Uses multiplication to convert
- `%.2f` formats output to 2 decimal places

---

## Question 13: Convert Celsius to Fahrenheit

**Answer:**

```c
#include <stdio.h>

int main() {
    float celsius, fahrenheit;
    
    printf("Enter temperature in Celsius: ");
    scanf("%f", &celsius);
    
    fahrenheit = (celsius * 9/5) + 32;
    printf("%.2f Celsius = %.2f Fahrenheit\n", celsius, fahrenheit);
    
    return 0;
}
```

**Explanation:**
- Formula: °F = (°C × 9/5) + 32
- Uses arithmetic operations to convert
- `9/5` is evaluated as integer division (1), so use `9.0/5.0` for better precision

---

## Question 14: Calculate area of rectangle

**Answer:**

```c
#include <stdio.h>

int main() {
    float length, width, area;
    
    printf("Enter length: ");
    scanf("%f", &length);
    printf("Enter width: ");
    scanf("%f", &width);
    
    area = length * width;
    printf("Area of rectangle = %.2f\n", area);
    
    return 0;
}
```

**Explanation:**
- Area = Length × Width
- Uses `float` for decimal precision
- Simple multiplication operation

---

## Question 15: Calculate area of circle

**Answer:**

```c
#include <stdio.h>
#define PI 3.14159

int main() {
    float radius, area;
    
    printf("Enter radius: ");
    scanf("%f", &radius);
    
    area = PI * radius * radius;
    printf("Area of circle = %.2f\n", area);
    
    return 0;
}
```

**Explanation:**
- Area = π × r²
- Uses `#define` to define PI constant
- `PI * radius * radius` calculates the area

---

## Question 16: Use getchar() and putchar() functions

**Answer:**

```c
#include <stdio.h>

int main() {
    char ch;
    
    printf("Enter a character: ");
    ch = getchar();
    
    printf("You entered: ");
    putchar(ch);
    printf("\n");
    
    return 0;
}
```

**Explanation:**
- `getchar()` reads a single character from input
- `putchar()` prints a single character to output
- These functions work with one character at a time

---

## Question 17: Print a simple pattern using *

**Answer:**

```c
#include <stdio.h>

int main() {
    int i, j;
    
    for(i = 1; i <= 5; i++) {
        for(j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }
    
    return 0;
}
```

**Output:**
```
* 
* * 
* * * 
* * * * 
* * * * * 
```

**Explanation:**
- Uses nested loops to create pattern
- Outer loop controls number of rows
- Inner loop prints stars in each row

---

## Question 18: Use escape sequences in printf

**Answer:**

```c
#include <stdio.h>

int main() {
    printf("Hello\n");           // New line
    printf("Tab\there\n");       // Tab
    printf("Backspace\b\n");     // Backspace
    printf("Carriage\rreturn\n"); // Carriage return
    printf("Double quote: \"Hello\"\n"); // Double quote
    printf("Single quote: \'A\'\n");     // Single quote
    printf("Backslash: \\\n");           // Backslash
    
    return 0;
}
```

**Explanation:**
- `\n` - New line
- `\t` - Tab
- `\b` - Backspace
- `\r` - Carriage return
- `\"` - Double quote
- `\'` - Single quote
- `\\` - Backslash

---

## Question 19: Create a calculator using basic operations

**Answer:**

```c
#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;
    
    printf("Enter an operator (+, -, *, /): ");
    scanf("%c", &operator);
    
    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);
    
    switch(operator) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            if(num2 != 0.0)
                result = num1 / num2;
            else {
                printf("Error: Division by zero!\n");
                return 1;
            }
            break;
        default:
            printf("Error: Invalid operator!\n");
            return 1;
    }
    
    printf("%.2lf %c %.2lf = %.2lf\n", num1, operator, num2, result);
    return 0;
}
```

**Explanation:**
- Uses `switch` statement for different operations
- Handles division by zero error
- Uses `double` for better precision
- `%lf` is format specifier for `double`

---

## Question 20: Take multiple inputs and print them

**Answer:**

```c
#include <stdio.h>

int main() {
    int a, b, c;
    float x, y;
    char ch;
    
    printf("Enter three integers: ");
    scanf("%d %d %d", &a, &b, &c);
    
    printf("Enter two float numbers: ");
    scanf("%f %f", &x, &y);
    
    printf("Enter a character: ");
    scanf(" %c", &ch);  // Note the space before %c
    
    printf("Integers: %d, %d, %d\n", a, b, c);
    printf("Floats: %.2f, %.2f\n", x, y);
    printf("Character: %c\n", ch);
    
    return 0;
}
```

**Explanation:**
- Multiple variables can be read in one `scanf()`
- Space before `%c` is important to skip whitespace
- Different format specifiers for different data types

---

## Question 21: Difference between = and ==

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 5;  // Assignment operator (=)
    int b = 10;
    
    if(a == b) {  // Comparison operator (==)
        printf("a equals b\n");
    } else {
        printf("a does not equal b\n");
    }
    
    // Common mistake
    if(a = b) {  // This assigns b to a and checks if a is non-zero
        printf("This will always execute if b is non-zero!\n");
    }
    
    return 0;
}
```

**Explanation:**
- `=` is assignment operator (assigns value)
- `==` is comparison operator (compares values)
- Using `=` instead of `==` in conditions is a common programming error

---

## Question 22: Use sizeof() operator

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 10;
    float b = 3.14;
    char c = 'A';
    double d = 3.14159;
    
    printf("Size of int variable: %zu bytes\n", sizeof(a));
    printf("Size of float variable: %zu bytes\n", sizeof(b));
    printf("Size of char variable: %zu bytes\n", sizeof(c));
    printf("Size of double variable: %zu bytes\n", sizeof(d));
    
    printf("Size of int type: %zu bytes\n", sizeof(int));
    printf("Size of float type: %zu bytes\n", sizeof(float));
    
    return 0;
}
```

**Explanation:**
- `sizeof()` can be used with variables or data types
- Returns size in bytes
- `%zu` is the correct format specifier for `size_t`

---

## Question 23: Create and use a constant

**Answer:**

```c
#include <stdio.h>

#define PI 3.14159
#define MAX_SIZE 100
#define GREETING "Hello, World!"

int main() {
    const int MIN_AGE = 18;
    const float TAX_RATE = 0.15;
    
    printf("PI = %.5f\n", PI);
    printf("MAX_SIZE = %d\n", MAX_SIZE);
    printf("GREETING: %s\n", GREETING);
    printf("MIN_AGE = %d\n", MIN_AGE);
    printf("TAX_RATE = %.2f\n", TAX_RATE);
    
    // PI = 3.14;  // This would cause error
    // MIN_AGE = 20;  // This would cause error
    
    return 0;
}
```

**Explanation:**
- `#define` creates preprocessor constants
- `const` creates compile-time constants
- Constants cannot be modified after declaration
- `#define` constants are replaced during preprocessing

---

## Question 24: Take float input with 2 decimal precision

**Answer:**

```c
#include <stdio.h>

int main() {
    float number;
    
    printf("Enter a float number: ");
    scanf("%f", &number);
    
    printf("Number with 2 decimal places: %.2f\n", number);
    printf("Number with 3 decimal places: %.3f\n", number);
    printf("Number with default precision: %f\n", number);
    
    return 0;
}
```

**Explanation:**
- `scanf("%f")` reads float input
- `%.2f` in `printf()` displays 2 decimal places
- `%.3f` displays 3 decimal places
- `%f` displays default precision (usually 6 decimal places)

---

## Question 25: Use comments in code

**Answer:**

```c
#include <stdio.h>

/* This is a multi-line comment
   It can span multiple lines
   Useful for detailed explanations */

int main() {
    // This is a single-line comment
    int a = 10;  // Inline comment
    
    /*
     * Another style of multi-line comment
     * Often used for function documentation
     */
    
    printf("Value of a: %d\n", a);
    
    return 0;  // Return success status
}
```

**Explanation:**
- `//` for single-line comments
- `/* */` for multi-line comments
- Comments are ignored by the compiler
- Good for explaining code logic and purpose

---

## Question 26: Explain return 0 in main

**Answer:**

```c
#include <stdio.h>

int main() {
    printf("Program executed successfully\n");
    return 0;  // Indicates successful execution
}

// Alternative main function
int main() {
    int result = some_operation();
    if(result < 0) {
        printf("Error occurred\n");
        return 1;  // Indicates error
    }
    return 0;  // Indicates success
}
```

**Explanation:**
- `return 0` indicates successful program execution
- `return 1` (or any non-zero value) indicates error
- Operating system uses this value to determine if program succeeded
- Convention: 0 = success, non-zero = error

---

## Question 27: What is a header file?

**Answer:**

```c
// stdio.h - Standard Input/Output header
#include <stdio.h>

// math.h - Mathematical functions header
#include <math.h>

// string.h - String manipulation functions header
#include <string.h>

// Custom header file example
#include "myheader.h"

int main() {
    printf("Using stdio.h functions\n");
    double result = sqrt(16.0);  // Using math.h function
    printf("Square root of 16: %.2f\n", result);
    return 0;
}
```

**Explanation:**
- Header files contain function declarations, macros, and constants
- `#include` directive includes header files
- `<header.h>` for system headers
- `"header.h"` for custom headers
- Headers provide interface to library functions

---

## Question 28: How to compile and run a C program?

**Answer:**

```bash
# Compile the program
gcc program.c -o program

# Run the program
./program

# Compile with warnings
gcc -Wall program.c -o program

# Compile with optimization
gcc -O2 program.c -o program

# Compile with debugging information
gcc -g program.c -o program
```

**Explanation:**
- `gcc` is the GNU C compiler
- `-o program` specifies output filename
- `-Wall` enables all warnings
- `-O2` enables optimization
- `-g` includes debugging information

---

## Question 29: Use clrscr() and getch() (Turbo C)

**Answer:**

```c
#include <stdio.h>
#include <conio.h>  // Required for clrscr() and getch()

int main() {
    printf("Press any key to clear screen...\n");
    getch();  // Wait for key press
    
    clrscr();  // Clear the screen
    
    printf("Screen cleared!\n");
    printf("Press any key to exit...\n");
    getch();  // Wait for key press before exiting
    
    return 0;
}
```

**Explanation:**
- `clrscr()` clears the console screen
- `getch()` waits for a key press
- These functions are specific to Turbo C/DOS
- Not available in standard C or modern compilers
- Use `system("cls")` (Windows) or `system("clear")` (Unix) as alternatives

---

## Question 30: Difference between main() and void main()

**Answer:**

```c
// Standard compliant main function
int main() {
    printf("This is standard compliant\n");
    return 0;  // Explicit return value
}

// Alternative standard compliant form
int main(int argc, char *argv[]) {
    printf("This accepts command line arguments\n");
    return 0;
}

// Non-standard form (not recommended)
void main() {
    printf("This is not standard compliant\n");
    // No return statement needed
}
```

**Explanation:**
- `int main()` is standard compliant (C89/C99/C11)
- `void main()` is not standard and may cause issues
- `int main()` must return an integer value
- `void main()` doesn't return anything
- Always use `int main()` for portability and standards compliance

---

## Summary

These 30 questions cover fundamental C programming concepts including:
- Basic input/output operations
- Data types and variables
- Arithmetic operations
- Control structures
- Functions and operators
- Constants and comments
- Compilation and execution
- Best practices and standards

Practice these examples to build a strong foundation in C programming! 