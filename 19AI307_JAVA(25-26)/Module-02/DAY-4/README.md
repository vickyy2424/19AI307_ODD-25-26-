# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to demonstrate the use of a default constructor and display a message from it.

## AIM:
To write a program to demonstrate the use of a default constructor and display a message from it.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class with a default constructor.
4.	Call the class from the main class.
5.	Stop the program. 





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:

```
import java.util.*;

class Student{
    
    Student(String name){
        System.out.println("Welcome, "+name+"! This is the default constructor.");
    }
}
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        new Student(name);
    }
}
```





## OUTPUT:
<img width="1223" height="346" alt="image" src="https://github.com/user-attachments/assets/5ef533f0-bcd8-4add-b913-4925eb6398c3" />



## RESULT:
Thus, the program to demonstrate the use of a default constructor and display a message from it was executed successfully and the output was verified.


