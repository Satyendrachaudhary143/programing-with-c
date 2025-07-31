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

---

## Question 31: Use arithmetic operators

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 10, b = 3;
    
    printf("a = %d, b = %d\n", a, b);
    printf("Addition: %d + %d = %d\n", a, b, a + b);
    printf("Subtraction: %d - %d = %d\n", a, b, a - b);
    printf("Multiplication: %d * %d = %d\n", a, b, a * b);
    printf("Division: %d / %d = %d\n", a, b, a / b);
    printf("Modulo: %d %% %d = %d\n", a, b, a % b);
    
    return 0;
}
```

**Explanation:**
- `+` : Addition operator
- `-` : Subtraction operator  
- `*` : Multiplication operator
- `/` : Division operator (integer division for integers)
- `%` : Modulo operator (remainder after division)

---

## Question 32: Use relational operators

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 10, b = 5;
    
    printf("a = %d, b = %d\n", a, b);
    printf("a == b: %d\n", a == b);  // Equal to
    printf("a != b: %d\n", a != b);  // Not equal to
    printf("a > b: %d\n", a > b);    // Greater than
    printf("a < b: %d\n", a < b);    // Less than
    printf("a >= b: %d\n", a >= b);  // Greater than or equal to
    printf("a <= b: %d\n", a <= b);  // Less than or equal to
    
    return 0;
}
```

**Explanation:**
- Relational operators return 1 (true) or 0 (false)
- `==` : Equal to
- `!=` : Not equal to
- `>` : Greater than
- `<` : Less than
- `>=` : Greater than or equal to
- `<=` : Less than or equal to

---

## Question 33: Use logical operators

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 1, b = 0;
    
    printf("a = %d, b = %d\n", a, b);
    printf("a && b: %d\n", a && b);  // Logical AND
    printf("a || b: %d\n", a || b);  // Logical OR
    printf("!a: %d\n", !a);          // Logical NOT
    printf("!b: %d\n", !b);          // Logical NOT
    
    return 0;
}
```

**Explanation:**
- `&&` : Logical AND (returns 1 if both operands are non-zero)
- `||` : Logical OR (returns 1 if at least one operand is non-zero)
- `!` : Logical NOT (returns 1 if operand is zero, 0 if non-zero)
- In C, any non-zero value is considered true, zero is false

---

## Question 34: Use bitwise operators

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 5, b = 3;  // 5 = 101, 3 = 011 in binary
    
    printf("a = %d (binary: 101), b = %d (binary: 011)\n", a, b);
    printf("a & b: %d (binary: 001)\n", a & b);   // Bitwise AND
    printf("a | b: %d (binary: 111)\n", a | b);   // Bitwise OR
    printf("a ^ b: %d (binary: 110)\n", a ^ b);   // Bitwise XOR
    printf("~a: %d\n", ~a);                       // Bitwise NOT
    printf("a << 1: %d (binary: 1010)\n", a << 1); // Left shift
    printf("a >> 1: %d (binary: 10)\n", a >> 1);   // Right shift
    
    return 0;
}
```

**Explanation:**
- `&` : Bitwise AND (1 if both bits are 1)
- `|` : Bitwise OR (1 if at least one bit is 1)
- `^` : Bitwise XOR (1 if bits are different)
- `~` : Bitwise NOT (inverts all bits)
- `<<` : Left shift (multiplies by 2^n)
- `>>` : Right shift (divides by 2^n)

---

## Question 35: Increment and decrement operator examples

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 5, b = 5;
    
    printf("Initial values: a = %d, b = %d\n", a, b);
    
    // Post-increment
    printf("a++: %d\n", a++);  // Prints 5, then increments to 6
    printf("After a++: a = %d\n", a);
    
    // Pre-increment
    printf("++b: %d\n", ++b);  // Increments to 6, then prints 6
    printf("After ++b: b = %d\n", b);
    
    // Post-decrement
    printf("a--: %d\n", a--);  // Prints 6, then decrements to 5
    printf("After a--: a = %d\n", a);
    
    // Pre-decrement
    printf("--b: %d\n", --b);  // Decrements to 5, then prints 5
    printf("After --b: b = %d\n", b);
    
    return 0;
}
```

**Explanation:**
- `++` : Increment operator
- `--` : Decrement operator
- `x++` : Post-increment (use value first, then increment)
- `++x` : Pre-increment (increment first, then use value)
- Same applies to decrement operators

---

## Question 36: Write program using compound assignment operators

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 10;
    
    printf("Initial value: a = %d\n", a);
    
    a += 5;  // Same as a = a + 5
    printf("After a += 5: a = %d\n", a);
    
    a -= 3;  // Same as a = a - 3
    printf("After a -= 3: a = %d\n", a);
    
    a *= 2;  // Same as a = a * 2
    printf("After a *= 2: a = %d\n", a);
    
    a /= 4;  // Same as a = a / 4
    printf("After a /= 4: a = %d\n", a);
    
    a %= 3;  // Same as a = a % 3
    printf("After a %%= 3: a = %d\n", a);
    
    a <<= 2; // Same as a = a << 2
    printf("After a <<= 2: a = %d\n", a);
    
    a >>= 1; // Same as a = a >> 1
    printf("After a >>= 1: a = %d\n", a);
    
    return 0;
}
```

**Explanation:**
- Compound assignment operators combine assignment with another operation
- `+=` : Add and assign
- `-=` : Subtract and assign
- `*=` : Multiply and assign
- `/=` : Divide and assign
- `%=` : Modulo and assign
- `<<=` : Left shift and assign
- `>>=` : Right shift and assign

---

## Question 37: Evaluate an expression using precedence

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 2, b = 3, c = 4;
    int result;
    
    printf("a = %d, b = %d, c = %d\n", a, b, c);
    
    // Expression: a + b * c
    result = a + b * c;
    printf("a + b * c = %d (multiplication has higher precedence)\n", result);
    
    // Expression: (a + b) * c
    result = (a + b) * c;
    printf("(a + b) * c = %d (parentheses override precedence)\n", result);
    
    // Expression: a * b + c / 2
    result = a * b + c / 2;
    printf("a * b + c / 2 = %d (* and / have same precedence, left to right)\n", result);
    
    return 0;
}
```

**Explanation:**
- Operator precedence determines order of evaluation
- Parentheses `()` have highest precedence
- `*`, `/`, `%` have higher precedence than `+`, `-`
- Same precedence operators are evaluated left to right
- Use parentheses to override default precedence

---

## Question 38: Explain difference between && and &

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 5, b = 3;
    
    printf("a = %d, b = %d\n", a, b);
    
    // Logical AND (&&)
    printf("a && b: %d (logical AND)\n", a && b);
    
    // Bitwise AND (&)
    printf("a & b: %d (bitwise AND)\n", a & b);
    
    // Example with zero
    int c = 0;
    printf("a = %d, c = %d\n", a, c);
    printf("a && c: %d (logical AND with zero)\n", a && c);
    printf("a & c: %d (bitwise AND with zero)\n", a & c);
    
    return 0;
}
```

**Explanation:**
- `&&` : Logical AND operator
  - Returns 1 (true) if both operands are non-zero
  - Returns 0 (false) if any operand is zero
  - Short-circuits (stops evaluation if first operand is false)
- `&` : Bitwise AND operator
  - Performs AND operation on each bit
  - Always evaluates both operands
  - Returns result based on bit patterns

---

## Question 39: Find even or odd using conditional operator

**Answer:**

```c
#include <stdio.h>

int main() {
    int number;
    
    printf("Enter a number: ");
    scanf("%d", &number);
    
    // Using conditional operator (ternary operator)
    printf("%d is %s\n", number, (number % 2 == 0) ? "even" : "odd");
    
    // Alternative using if-else
    if(number % 2 == 0) {
        printf("%d is even\n", number);
    } else {
        printf("%d is odd\n", number);
    }
    
    return 0;
}
```

**Explanation:**
- Conditional operator: `condition ? expression1 : expression2`
- If condition is true, evaluates expression1
- If condition is false, evaluates expression2
- `number % 2 == 0` checks if number is even
- More concise than if-else for simple conditions

---

## Question 40: Convert decimal to binary using bitwise shift

**Answer:**

```c
#include <stdio.h>

int main() {
    int decimal, i;
    
    printf("Enter a decimal number: ");
    scanf("%d", &decimal);
    
    printf("Binary representation of %d: ", decimal);
    
    // Print binary using bitwise operations
    for(i = 31; i >= 0; i--) {
        printf("%d", (decimal >> i) & 1);
    }
    printf("\n");
    
    // Alternative: print only significant bits
    printf("Binary (significant bits): ");
    int found_one = 0;
    for(i = 31; i >= 0; i--) {
        int bit = (decimal >> i) & 1;
        if(bit == 1) found_one = 1;
        if(found_one) printf("%d", bit);
    }
    printf("\n");
    
    return 0;
}
```

**Explanation:**
- `(decimal >> i) & 1` extracts the i-th bit
- Right shift moves bits to the right
- `& 1` masks all bits except the least significant bit
- Loop from 31 to 0 prints all 32 bits
- Second loop prints only significant bits (skips leading zeros)

---

## Question 41: Demonstrate short-circuit evaluation

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 5, b = 0;
    
    printf("a = %d, b = %d\n", a, b);
    
    // Logical AND short-circuit
    printf("Testing: a && b\n");
    if(a && b) {
        printf("Both conditions are true\n");
    } else {
        printf("Short-circuit: b is not evaluated because a is non-zero\n");
    }
    
    // Logical OR short-circuit
    printf("Testing: a || b\n");
    if(a || b) {
        printf("Short-circuit: b is not evaluated because a is non-zero\n");
    } else {
        printf("Both conditions are false\n");
    }
    
    // Demonstrate with function calls
    printf("Testing: a && (printf(\"This won't print\\n\"), 0)\n");
    if(a && (printf("This won't print\n"), 0)) {
        printf("This will print\n");
    }
    
    return 0;
}
```

**Explanation:**
- Short-circuit evaluation stops as soon as the result is determined
- For `&&`: if first operand is false, second is not evaluated
- For `||`: if first operand is true, second is not evaluated
- This can improve performance and prevent errors
- Useful for avoiding division by zero, null pointer access, etc.

---

## Question 42: Use sizeof with expression

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 10;
    double b = 3.14;
    char c = 'A';
    
    printf("Size of variable a: %zu bytes\n", sizeof(a));
    printf("Size of expression a + 5: %zu bytes\n", sizeof(a + 5));
    printf("Size of expression a + b: %zu bytes\n", sizeof(a + b));
    
    printf("Size of literal 100: %zu bytes\n", sizeof(100));
    printf("Size of literal 3.14: %zu bytes\n", sizeof(3.14));
    printf("Size of literal 'A': %zu bytes\n", sizeof('A'));
    
    printf("Size of array int[5]: %zu bytes\n", sizeof(int[5]));
    printf("Size of pointer: %zu bytes\n", sizeof(int*));
    
    return 0;
}
```

**Explanation:**
- `sizeof()` can be used with variables, expressions, or types
- Returns the size in bytes
- For expressions, evaluates the type but doesn't execute the expression
- `sizeof(int[5])` returns size of array of 5 integers
- `sizeof(int*)` returns size of pointer to integer

---

## Question 43: Find power using bitwise left shift

**Answer:**

```c
#include <stdio.h>

int main() {
    int base = 2, power;
    
    printf("Enter power of 2: ");
    scanf("%d", &power);
    
    // Using left shift: 2^n = 1 << n
    int result = 1 << power;
    printf("2^%d = %d\n", power, result);
    
    // Verify with multiplication
    int verify = 1;
    for(int i = 0; i < power; i++) {
        verify *= 2;
    }
    printf("Verification: 2^%d = %d\n", power, verify);
    
    // Powers of 2 from 0 to 10
    printf("Powers of 2:\n");
    for(int i = 0; i <= 10; i++) {
        printf("2^%d = %d\n", i, 1 << i);
    }
    
    return 0;
}
```

**Explanation:**
- Left shift by n positions multiplies by 2^n
- `1 << n` gives 2^n
- More efficient than multiplication for powers of 2
- Limited to powers of 2 (not general exponentiation)
- Useful for bit manipulation and optimization

---

## Question 44: Toggle a bit using XOR

**Answer:**

```c
#include <stdio.h>

int main() {
    int num = 10;  // Binary: 1010
    int position;
    
    printf("Original number: %d (binary: 1010)\n", num);
    printf("Enter bit position to toggle (0-31): ");
    scanf("%d", &position);
    
    // Toggle bit using XOR
    int mask = 1 << position;
    num = num ^ mask;
    
    printf("After toggling bit %d: %d\n", position, num);
    
    // Show binary representation
    printf("Binary representation: ");
    for(int i = 31; i >= 0; i--) {
        printf("%d", (num >> i) & 1);
    }
    printf("\n");
    
    return 0;
}
```

**Explanation:**
- XOR with 1 toggles a bit (0 becomes 1, 1 becomes 0)
- `1 << position` creates a mask with 1 at the specified position
- `num ^ mask` toggles the bit at that position
- XOR properties: `0 ^ 1 = 1`, `1 ^ 1 = 0`
- Useful for bit manipulation and flags

---

## Question 45: Explain difference between a = b++ and a = ++b

**Answer:**

```c
#include <stdio.h>

int main() {
    int b = 5;
    int a;
    
    printf("Initial value: b = %d\n", b);
    
    // Post-increment assignment
    a = b++;  // a gets the value of b (5), then b is incremented to 6
    printf("After a = b++: a = %d, b = %d\n", a, b);
    
    // Reset b
    b = 5;
    
    // Pre-increment assignment
    a = ++b;  // b is incremented to 6, then a gets the value of b (6)
    printf("After a = ++b: a = %d, b = %d\n", a, b);
    
    return 0;
}
```

**Explanation:**
- `a = b++` : Post-increment assignment
  - Assigns current value of b to a
  - Then increments b
- `a = ++b` : Pre-increment assignment
  - Increments b first
  - Then assigns new value of b to a
- Both increment b, but differ in when the increment happens

---

## Question 46: Use ternary operator

**Answer:**

```c
#include <stdio.h>

int main() {
    int age;
    
    printf("Enter your age: ");
    scanf("%d", &age);
    
    // Simple ternary operator
    printf("You are %s\n", (age >= 18) ? "an adult" : "a minor");
    
    // Nested ternary operator
    printf("Category: %s\n", 
           (age < 13) ? "child" : 
           (age < 20) ? "teenager" : 
           (age < 65) ? "adult" : "senior");
    
    // Ternary with arithmetic
    int max = (age > 25) ? age : 25;
    printf("Maximum value: %d\n", max);
    
    // Ternary with different data types
    printf("Status: %s\n", (age >= 18) ? "eligible" : "not eligible");
    
    return 0;
}
```

**Explanation:**
- Ternary operator: `condition ? expression1 : expression2`
- Compact alternative to if-else
- Can be nested for multiple conditions
- Both expressions should be of compatible types
- Useful for simple conditional assignments

---

## Question 47: Demonstrate logical NOT

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 5, b = 0;
    
    printf("a = %d, b = %d\n", a, b);
    printf("!a = %d\n", !a);  // 0 (false)
    printf("!b = %d\n", !b);  // 1 (true)
    
    // Using logical NOT in conditions
    if(!a) {
        printf("a is zero\n");
    } else {
        printf("a is non-zero\n");
    }
    
    if(!b) {
        printf("b is zero\n");
    } else {
        printf("b is non-zero\n");
    }
    
    // Double negation
    printf("!!a = %d\n", !!a);  // 1 (true)
    printf("!!b = %d\n", !!b);  // 0 (false)
    
    return 0;
}
```

**Explanation:**
- `!` operator negates the logical value
- `!0` = 1 (true)
- `!non_zero` = 0 (false)
- `!!` double negation converts to boolean (0 or 1)
- Useful for checking if a value is zero or non-zero

---

## Question 48: Operator to check if number is power of 2

**Answer:**

```c
#include <stdio.h>

int main() {
    int num;
    
    printf("Enter a number: ");
    scanf("%d", &num);
    
    // Method 1: Using bitwise AND
    if(num > 0 && (num & (num - 1)) == 0) {
        printf("%d is a power of 2\n", num);
    } else {
        printf("%d is not a power of 2\n", num);
    }
    
    // Method 2: Using loop
    int temp = num;
    int is_power_of_2 = 1;
    
    if(num <= 0) {
        is_power_of_2 = 0;
    } else {
        while(temp > 1) {
            if(temp % 2 != 0) {
                is_power_of_2 = 0;
                break;
            }
            temp /= 2;
        }
    }
    
    printf("Method 2 result: %d is %s\n", num, 
           is_power_of_2 ? "a power of 2" : "not a power of 2");
    
    return 0;
}
```

**Explanation:**
- Power of 2 has exactly one bit set to 1
- `num & (num - 1)` removes the least significant 1 bit
- If result is 0, number has only one 1 bit (power of 2)
- Example: 8 (1000) & 7 (0111) = 0
- More efficient than division method

---

## Question 49: Find maximum of three numbers using ternary

**Answer:**

```c
#include <stdio.h>

int main() {
    int a, b, c;
    
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    
    // Using nested ternary operator
    int max = (a > b) ? ((a > c) ? a : c) : ((b > c) ? b : c);
    
    printf("Maximum of %d, %d, %d is %d\n", a, b, c, max);
    
    // Alternative using if-else
    int max2;
    if(a > b) {
        max2 = (a > c) ? a : c;
    } else {
        max2 = (b > c) ? b : c;
    }
    
    printf("Maximum (alternative): %d\n", max2);
    
    return 0;
}
```

**Explanation:**
- Nested ternary operator: `condition1 ? expression1 : (condition2 ? expression2 : expression3)`
- Compares a with b first, then compares the larger with c
- More compact than if-else but can be harder to read
- Useful for simple conditional logic

---

## Question 50: Swap variables using XOR

**Answer:**

```c
#include <stdio.h>

int main() {
    int a, b;
    
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    
    printf("Before swap: a = %d, b = %d\n", a, b);
    
    // Swap using XOR
    a = a ^ b;
    b = a ^ b;
    a = a ^ b;
    
    printf("After swap: a = %d, b = %d\n", a, b);
    
    // Verify with arithmetic method
    int x = 10, y = 20;
    printf("Before swap: x = %d, y = %d\n", x, y);
    
    x = x + y;
    y = x - y;
    x = x - y;
    
    printf("After swap: x = %d, y = %d\n", x, y);
    
    return 0;
}
```

**Explanation:**
- XOR swap: `a = a ^ b; b = a ^ b; a = a ^ b;`
- Works because XOR is associative and commutative
- `a ^ a = 0` and `a ^ 0 = a`
- No temporary variable needed
- Can cause issues if a and b point to same memory location

---

## Question 51: Use modulo operator

**Answer:**

```c
#include <stdio.h>

int main() {
    int dividend, divisor;
    
    printf("Enter dividend: ");
    scanf("%d", &dividend);
    printf("Enter divisor: ");
    scanf("%d", &divisor);
    
    if(divisor != 0) {
        int quotient = dividend / divisor;
        int remainder = dividend % divisor;
        
        printf("Quotient: %d\n", quotient);
        printf("Remainder: %d\n", remainder);
        printf("Verification: %d = %d * %d + %d\n", 
               dividend, divisor, quotient, remainder);
    } else {
        printf("Error: Division by zero!\n");
    }
    
    // Common uses of modulo
    printf("Last digit of %d: %d\n", dividend, dividend % 10);
    printf("Is %d even? %s\n", dividend, (dividend % 2 == 0) ? "Yes" : "No");
    
    return 0;
}
```

**Explanation:**
- `%` operator returns remainder after division
- `dividend = divisor * quotient + remainder`
- Useful for:
  - Finding last digit (mod 10)
  - Checking even/odd (mod 2)
  - Circular arrays (mod array_size)
  - Time calculations (mod 24, mod 60)

---

## Question 52: Compound assignment inside loop

**Answer:**

```c
#include <stdio.h>

int main() {
    int sum = 0, product = 1;
    int n;
    
    printf("Enter number of elements: ");
    scanf("%d", &n);
    
    printf("Enter %d numbers:\n", n);
    
    for(int i = 0; i < n; i++) {
        int num;
        scanf("%d", &num);
        
        // Compound assignments in loop
        sum += num;      // Same as sum = sum + num
        product *= num;  // Same as product = product * num
    }
    
    printf("Sum: %d\n", sum);
    printf("Product: %d\n", product);
    
    // Another example with bitwise operations
    int result = 0;
    for(int i = 0; i < 5; i++) {
        result |= (1 << i);  // Set i-th bit
        printf("After setting bit %d: %d\n", i, result);
    }
    
    return 0;
}
```

**Explanation:**
- Compound assignment operators are useful in loops
- `+=` for accumulating sums
- `*=` for accumulating products
- `|=` for setting bits
- `&=` for clearing bits
- More concise and often more efficient than separate operations

---

## Question 53: Write complex expression with all operators

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 10, b = 5, c = 3;
    int result;
    
    printf("a = %d, b = %d, c = %d\n", a, b, c);
    
    // Complex expression with multiple operators
    result = (a + b * c) & ((a - b) | (c << 2)) ^ (a % b);
    printf("Complex expression result: %d\n", result);
    
    // Break down the expression
    int step1 = b * c;           // 5 * 3 = 15
    int step2 = a + step1;       // 10 + 15 = 25
    int step3 = a - b;           // 10 - 5 = 5
    int step4 = c << 2;          // 3 << 2 = 12
    int step5 = step3 | step4;   // 5 | 12 = 13
    int step6 = a % b;           // 10 % 5 = 0
    int step7 = step2 & step5;   // 25 & 13 = 9
    int final_result = step7 ^ step6; // 9 ^ 0 = 9
    
    printf("Step-by-step breakdown:\n");
    printf("b * c = %d\n", step1);
    printf("a + (b * c) = %d\n", step2);
    printf("a - b = %d\n", step3);
    printf("c << 2 = %d\n", step4);
    printf("(a - b) | (c << 2) = %d\n", step5);
    printf("a %% b = %d\n", step6);
    printf("(a + b * c) & ((a - b) | (c << 2)) = %d\n", step7);
    printf("Final result = %d\n", final_result);
    
    return 0;
}
```

**Explanation:**
- Expression combines arithmetic, bitwise, and logical operators
- Operator precedence determines evaluation order
- Parentheses override default precedence
- Complex expressions should be broken down for clarity
- Use parentheses to make precedence explicit

---

## Question 54: Use comma operator in an expression

**Answer:**

```c
#include <stdio.h>

int main() {
    int a, b, c;
    
    // Comma operator in variable declaration
    a = 1, b = 2, c = 3;
    printf("a = %d, b = %d, c = %d\n", a, b, c);
    
    // Comma operator in for loop
    for(int i = 0, j = 10; i < 5; i++, j--) {
        printf("i = %d, j = %d\n", i, j);
    }
    
    // Comma operator in expression
    int result = (a = 5, b = 10, a + b);
    printf("Result: %d\n", result);
    
    // Comma operator with function calls
    int x = (printf("Hello "), printf("World\n"), 42);
    printf("x = %d\n", x);
    
    // Comma operator in conditional
    int y = 5;
    if(y > 3, y < 10) {
        printf("Condition is true (value of y < 10)\n");
    }
    
    return 0;
}
```

**Explanation:**
- Comma operator `,` evaluates expressions from left to right
- Returns the value of the rightmost expression
- Useful for:
  - Multiple expressions in for loop
  - Multiple assignments in one statement
  - Side effects in expressions
- Lowest precedence of all operators

---

## Question 55: Nest multiple ternary operations

**Answer:**

```c
#include <stdio.h>

int main() {
    int score;
    
    printf("Enter your score (0-100): ");
    scanf("%d", &score);
    
    // Nested ternary for grade calculation
    char grade = (score >= 90) ? 'A' : 
                 (score >= 80) ? 'B' : 
                 (score >= 70) ? 'C' : 
                 (score >= 60) ? 'D' : 'F';
    
    printf("Grade: %c\n", grade);
    
    // Nested ternary for number comparison
    int a = 10, b = 20, c = 15;
    int max = (a > b) ? ((a > c) ? a : c) : ((b > c) ? b : c);
    int min = (a < b) ? ((a < c) ? a : c) : ((b < c) ? b : c);
    
    printf("Numbers: %d, %d, %d\n", a, b, c);
    printf("Maximum: %d\n", max);
    printf("Minimum: %d\n", min);
    
    // Nested ternary for string output
    printf("Status: %s\n", 
           (score >= 90) ? "Excellent" :
           (score >= 80) ? "Good" :
           (score >= 70) ? "Average" :
           (score >= 60) ? "Below Average" : "Fail");
    
    return 0;
}
```

**Explanation:**
- Nested ternary operators: `condition1 ? expr1 : (condition2 ? expr2 : expr3)`
- Evaluates from right to left
- Can be used for multiple conditions
- More compact than if-else chains
- Can become hard to read with many levels

---

## Question 56: Priority of logical operators

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 1, b = 0, c = 1;
    
    printf("a = %d, b = %d, c = %d\n", a, b, c);
    
    // Demonstrating operator precedence
    int result1 = a && b || c;
    printf("a && b || c = %d\n", result1);
    
    int result2 = (a && b) || c;
    printf("(a && b) || c = %d\n", result2);
    
    int result3 = a && (b || c);
    printf("a && (b || c) = %d\n", result3);
    
    // Precedence order: ! > && > ||
    int result4 = !a && b || c;
    printf("!a && b || c = %d\n", result4);
    
    int result5 = !(a && b) || c;
    printf("!(a && b) || c = %d\n", result5);
    
    return 0;
}
```

**Explanation:**
- Logical operator precedence (highest to lowest):
  1. `!` (logical NOT)
  2. `&&` (logical AND)
  3. `||` (logical OR)
- Use parentheses to override precedence
- `&&` has higher precedence than `||`
- Always use parentheses for clarity in complex expressions

---

## Question 57: Convert negative number to binary

**Answer:**

```c
#include <stdio.h>

int main() {
    int num;
    
    printf("Enter a number: ");
    scanf("%d", &num);
    
    printf("Number: %d\n", num);
    
    // Method 1: Using bitwise operations
    printf("Binary representation: ");
    for(int i = 31; i >= 0; i--) {
        printf("%d", (num >> i) & 1);
    }
    printf("\n");
    
    // Method 2: Using unsigned int to avoid sign issues
    unsigned int unum = (unsigned int)num;
    printf("Binary (unsigned): ");
    for(int i = 31; i >= 0; i--) {
        printf("%d", (unum >> i) & 1);
    }
    printf("\n");
    
    // Show two's complement for negative numbers
    if(num < 0) {
        printf("Two's complement representation:\n");
        printf("Original: ");
        for(int i = 31; i >= 0; i--) {
            printf("%d", ((-num) >> i) & 1);
        }
        printf("\n");
        printf("Inverted + 1: ");
        for(int i = 31; i >= 0; i--) {
            printf("%d", (num >> i) & 1);
        }
        printf("\n");
    }
    
    return 0;
}
```

**Explanation:**
- Negative numbers use two's complement representation
- To get negative: invert all bits and add 1
- Right shift preserves sign bit for negative numbers
- Cast to unsigned to see actual bit pattern
- 32-bit integers use 31 bits for magnitude, 1 for sign

---

## Question 58: Demonstrate use of ! operator

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 5, b = 0;
    
    printf("a = %d, b = %d\n", a, b);
    
    // Basic logical NOT
    printf("!a = %d\n", !a);
    printf("!b = %d\n", !b);
    
    // Using ! in conditions
    if(!a) {
        printf("a is zero\n");
    } else {
        printf("a is non-zero\n");
    }
    
    if(!b) {
        printf("b is zero\n");
    } else {
        printf("b is non-zero\n");
    }
    
    // Double negation
    printf("!!a = %d\n", !!a);
    printf("!!b = %d\n", !!b);
    
    // ! with comparison operators
    printf("!(a > 3) = %d\n", !(a > 3));
    printf("!(b == 0) = %d\n", !(b == 0));
    
    // ! with logical operators
    printf("!(a && b) = %d\n", !(a && b));
    printf("!(a || b) = %d\n", !(a || b));
    
    return 0;
}
```

**Explanation:**
- `!` operator negates the logical value
- `!0` = 1 (true)
- `!non_zero` = 0 (false)
- Can be used with any expression
- `!!` converts to boolean (0 or 1)
- Useful for checking zero/non-zero conditions

---

## Question 59: Operator used to check parity

**Answer:**

```c
#include <stdio.h>

int main() {
    int num;
    
    printf("Enter a number: ");
    scanf("%d", &num);
    
    // Method 1: Using modulo operator
    if(num % 2 == 0) {
        printf("%d is even\n", num);
    } else {
        printf("%d is odd\n", num);
    }
    
    // Method 2: Using bitwise AND
    if((num & 1) == 0) {
        printf("%d is even (bitwise check)\n", num);
    } else {
        printf("%d is odd (bitwise check)\n", num);
    }
    
    // Method 3: Using ternary operator
    printf("%d is %s\n", num, (num % 2 == 0) ? "even" : "odd");
    
    // Check multiple numbers
    printf("Parity check for numbers 1-10:\n");
    for(int i = 1; i <= 10; i++) {
        printf("%d: %s\n", i, (i & 1) ? "odd" : "even");
    }
    
    return 0;
}
```

**Explanation:**
- Parity refers to whether a number is even or odd
- `num % 2 == 0` checks if remainder is 0 (even)
- `num & 1 == 0` checks if least significant bit is 0 (even)
- Bitwise method is more efficient
- Both methods work for positive and negative numbers

---

## Question 60: Use sizeof(a++) – does a++ execute?

**Answer:**

```c
#include <stdio.h>

int main() {
    int a = 5;
    
    printf("Before sizeof(a++): a = %d\n", a);
    
    // sizeof(a++) - a++ is NOT executed
    size_t size = sizeof(a++);
    printf("sizeof(a++) = %zu\n", size);
    printf("After sizeof(a++): a = %d (unchanged!)\n", a);
    
    // Compare with actual increment
    printf("Before a++: a = %d\n", a);
    a++;
    printf("After a++: a = %d\n", a);
    
    // sizeof with different expressions
    printf("sizeof(a + 1) = %zu\n", sizeof(a + 1));
    printf("sizeof(a = 10) = %zu\n", sizeof(a = 10));
    printf("a is still: %d\n", a);
    
    return 0;
}
```

**Explanation:**
- `sizeof()` is a compile-time operator
- The expression inside `sizeof()` is NOT evaluated
- Only the type of the expression is determined
- `sizeof(a++)` returns size of int, doesn't increment a
- This is because `sizeof()` operates on types, not values
- Useful for avoiding side effects in expressions

---

## Summary

These 60 questions cover comprehensive C programming concepts including:
- Basic input/output operations
- Data types and variables
- Arithmetic, relational, logical, and bitwise operators
- Control structures and loops
- Functions and operators
- Constants, comments, and compilation
- Advanced operator concepts and precedence
- Bit manipulation and optimization techniques
- Best practices and standards

Practice these examples to build a strong foundation in C programming! 