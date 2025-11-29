# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.

## AIM:
To write a Java program to convert a string to an integer using a wrapper class and perform addition.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Get the input from the user.
4.	Use Wrapper class to convert it into integer.
5.	Sum and print it.
6.	Stop the program. 





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String inputString = sc.nextLine();
        
        int number1 = Integer.parseInt(inputString);
        
        int number2 = sc.nextInt();
        
        int sum = number1 + number2;
        
        System.out.println("Sum = " + sum);
    }
}
```






## OUTPUT:
<img width="1224" height="428" alt="image" src="https://github.com/user-attachments/assets/ab46f641-2f72-4022-b66d-74fbe6f6cfea" />



## RESULT:
The program successfully used Integer wrapper class in conditional logic. It correctly evaluated sums the integers and prints the output. 


