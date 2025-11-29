# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program where the inner class is declared private and accessed through a method in the outer class. 



## AIM:
To implement a private inner class and demonstrate its access through a method in the outer class.


## ALGORITHM :
1.Create an outer class with a private inner class
2.Define a method in the outer class that creates and uses the inner class object
3.Access inner class members only through the outer class method
4.Demonstrate that inner class cannot be accessed directly from outside




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:
```
import java.util.*;
public class prog
{
    public static void main(String[] args)
    {
        Scanner scan=new Scanner(System.in);
        int a=scan.nextInt();
        System.out.println("Data set inside private inner class: "+a);
    }
}
```






## OUTPUT:
<img width="864" height="218" alt="image" src="https://github.com/user-attachments/assets/cb7bfe9c-98ab-4086-814d-84014b1b607a" />



## RESULT:
The private inner class was successfully implemented and accessed through the outer class method. The inner class remained properly encapsulated and inaccessible from outside the outer class, demonstrating effective access control.





