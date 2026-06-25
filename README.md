# Java Calculator

A simple calculator program in Java that performs basic arithmetic operations such as Addition (+), Subtraction (-), Multiplication (*), Division (/), and Modulus (%).

## Features

* Addition
* Subtraction
* Multiplication
* Division
* Modulus
* Handles division by zero
* Handles invalid operators

## Code

```java
import java.util.*;

public class Calculator {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Read first number
        double num1 = sc.nextDouble();

        // Read operator
        char operator = sc.next().charAt(0);

        // Read second number
        double num2 = sc.nextDouble();

        double result = 0;

        // Perform calculation based on operator
        if (operator == '+') {
            result = num1 + num2;
        }
        else if (operator == '-') {
            result = num1 - num2;
        }
        else if (operator == '*') {
            result = num1 * num2;
        }
        else if (operator == '/') {
            if (num2 != 0) {
                result = num1 / num2;
            } else {
                System.out.println("Division by zero not allowed");
                return;
            }
        }
        else if (operator == '%') {
            if (num2 != 0) {
                result = num1 % num2;
            } else {
                System.out.println("Modulo by zero not allowed");
                return;
            }
        }
        else {
            System.out.println("Invalid mathematical operator choice");
            return;
        }

        System.out.println("Result: " + result);

        sc.close();
    }
}
```

## Sample Input

```
10 + 5
```

## Sample Output

```
Result: 15.0
```

## Author

Rithika Krishnamoorthy
