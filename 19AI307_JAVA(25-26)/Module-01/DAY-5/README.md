# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to swap two strings without using a third variable.

## AIM:
To write a Java program to swap two strings without using a third variable.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Get the input from the user.
4.	Add both the string in the string a.
5.	String b is a substring of length of a - length of b.
6.	String a is now a substring of the remaining characters.
7.	Stop the program. 





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:

```
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        String a = sc.nextLine();
        String b = sc.nextLine();
        
        a = a + b;
        b = a.substring(0, a.length() - b.length());
        a = a.substring(b.length());
        
        System.out.println("After swapping:");
        System.out.println("First string (A): "+a);
        System.out.println("Second string (B): "+b);
    }
}
```





## OUTPUT:
<img width="1217" height="479" alt="image" src="https://github.com/user-attachments/assets/5b4c5a97-a1e7-443f-b40d-6747dd7ec00d" />


## RESULT:
Thus a Java program to swap two strings without using a third variable is written and all the test cases passes successfully. 


