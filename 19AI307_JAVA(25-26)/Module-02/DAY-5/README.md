# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## AIM:
To create a Calculator class with both non-static and static methods and demonstrate their usage.


## ALGORITHM :
1.Create Calculator class with non-static add() method that returns sum of two integers
2.Create static info() method that displays ready message
3.In main method, call static method using class name
4.Create object and call non-static add() method using object reference




## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Calculator {
    public int add(int a, int b) {
        return a + b;
    }

    public static void info() {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num1 = sc.nextInt();
        int num2 = sc.nextInt();

        Calculator.info();

        Calculator calc = new Calculator();
        int sum = calc.add(num1, num2);
        System.out.println("Sum: " + sum);

        sc.close();
    }
}
```






## OUTPUT:

<img width="570" height="280" alt="image" src="https://github.com/user-attachments/assets/0f358a52-ab30-42f3-99ed-e7a052e47202" />



## RESULT:
The Calculator class was successfully implemented. The static info() method was accessed without object creation, and the non-static add() method worked correctly when called through an object instance, demonstrating proper usage of both static and non-static methods.




