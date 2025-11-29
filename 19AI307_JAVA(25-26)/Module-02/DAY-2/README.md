# Ex.No:2(B) METHODS

## QUESTION:
Write a class with one static method and one non-static method. Call both from the main() method.

## AIM:
To write a class with one static method and one non-static method. Call both from the main() method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create two methods, one static and one non static.
4.	Call both the methods.
5.	Stop the program. 





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:

```
public class Main{
    public static void main(String[] args){
        staticMethod();
        Main obj = new Main();
        obj.nonStaticMethod();
    }
    static void staticMethod(){
        System.out.println("I am static");
    }
    void nonStaticMethod(){
        System.out.println("I am non-static");
    }
    
}
```





## OUTPUT:
<img width="1232" height="287" alt="image" src="https://github.com/user-attachments/assets/364c7006-b038-487f-a174-70e4f19f54e1" />



## RESULT:
Thus a Java program to Write a class with one static method and one non-static method, and call both from the main() method is written and passes all the test cases. 



