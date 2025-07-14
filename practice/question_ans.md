# Question 1: Number Swapper Using C

**Question:** Write a C program to swap two numbers. Explain the code in detail.

---

## Answer

Swapping two numbers means exchanging their values. For example, if `a = 5` and `b = 10`, after swapping, `a` should be `10` and `b` should be `5`.

### C Program to Swap Two Numbers

```c
#include <stdio.h>

int main() {
    int a, b, temp;
    printf("Enter first number: ");
    scanf("%d", &a);
    printf("Enter second number: ");
    scanf("%d", &b);

    // Swapping logic
    temp = a;
    a = b;
    b = temp;

    printf("After swapping, first number = %d\n", a);
    printf("After swapping, second number = %d\n", b);
    return 0;
}
```

### Explanation
1. **Variable Declaration:**
   - `int a, b, temp;` declares three integer variables. `a` and `b` store the numbers to be swapped, and `temp` is a temporary variable used for swapping.
2. **Input:**
   - The program asks the user to enter two numbers using `printf` and reads them using `scanf`.
3. **Swapping Logic:**
   - `temp = a;` stores the value of `a` in `temp`.
   - `a = b;` assigns the value of `b` to `a`.
   - `b = temp;` assigns the value stored in `temp` (original value of `a`) to `b`.
4. **Output:**
   - The program prints the values of `a` and `b` after swapping.

---

## Swapping Without Using a Temporary Variable

It is also possible to swap two numbers without using a third (temporary) variable. This can be done using arithmetic operations or bitwise XOR.

### Method 1: Using Arithmetic Operators

```c
#include <stdio.h>

int main() {
    int a, b;
    printf("Enter first number: ");
    scanf("%d", &a);
    printf("Enter second number: ");
    scanf("%d", &b);

    // Swapping without temp
    a = a + b;
    b = a - b;
    a = a - b;

    printf("After swapping, first number = %d\n", a);
    printf("After swapping, second number = %d\n", b);
    return 0;
}
```

#### Explanation
1. `a = a + b;` // Now a holds the sum of a and b
2. `b = a - b;` // Subtract original b from sum to get original a
3. `a = a - b;` // Subtract new b (original a) from sum to get original b

---

### Method 2: Using Bitwise XOR Operator

```c
#include <stdio.h>

int main() {
    int a, b;
    printf("Enter first number: ");
    scanf("%d", &a);
    printf("Enter second number: ");
    scanf("%d", &b);

    // Swapping using XOR
    a = a ^ b;
    b = a ^ b;
    a = a ^ b;

    printf("After swapping, first number = %d\n", a);
    printf("After swapping, second number = %d\n", b);
    return 0;
}
```

#### Explanation
- The XOR method swaps values without using extra space. Each XOR operation manipulates the bits so that the values are exchanged.

---

**Note:** These methods work for integers. The arithmetic method may cause overflow if the sum exceeds the range of `int`. The XOR method is safe for integers but should not be used for floating-point numbers. 