[# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Write a Java program to check how strong is the given code. 

## AIM:
To write a Java program to check how strong is the given code. 

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Get the input from the user.
4.	Based on the condition print the statements.
5.	End the program. 





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Vigneshwarn S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        if(a%2==0 && a<100){
            System.out.print("Weak Code");
        }
        else if(a%2==0 && a>100 && a<999){
            System.out.print("Strong Code");
        }
        else{
            System.out.print("Access Denied");
        }
    }
}
```






## OUTPUT:

<img width="1274" height="398" alt="image" src="https://github.com/user-attachments/assets/950acbd3-3935-4195-bd47-f0689734fe8f" />


## RESULT:
The Java program successfully implements the code logic and produces correct outputs for all test cases as per the given rules.




](https://meet.google.com/hdi-quva-oyy?authuser=0)
