# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You have a program that reads an integer from the user. The program must reject any negative number by throwing a special error.How would you design a custom exception to handle this? What message would you display if the user enters a negative number?

## AIM:
To Accept valid numbers and throw error when a negative number is entered. 

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Use try-catch block to handle negative numbers.
4.	Catch NegativeNumberException for negative numbers.
5.	Display result or error message accordingly





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class NegativeNumberException extends Exception {
    public NegativeNumberException(String message) {
        super(message);
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        try {
            if (num < 0) {
                throw new NegativeNumberException("Negative numbers are not allowed");
            }
            System.out.println("Valid input: " + num);
        } catch (NegativeNumberException e) {
            System.out.println(e.getMessage());
        }

        sc.close();
    }
}

```





## OUTPUT:
<img width="1265" height="415" alt="image" src="https://github.com/user-attachments/assets/15e3d756-8cf7-45fb-86ea-a488a390fb22" />



## RESULT:
The Java program has handled the negative number entry scenario by using the NegativeNumberException and passes all the test cases. 


