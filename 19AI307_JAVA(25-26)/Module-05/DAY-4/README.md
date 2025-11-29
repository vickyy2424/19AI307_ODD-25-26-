# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

## AIM:
To write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create multiple thread objects in main method
4. Start threads using start() method
5. Observe concurrent execution





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:

```
import java.util.*;

public class TwoThreadPriority {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name1 = sc.nextLine();
        String name2 = sc.nextLine();

        Thread t1 = new Thread();
        t1.setName(name1);
        t1.setPriority(4);

        Thread t2 = new Thread();
        t2.setName(name2);
        t2.setPriority(2);

        System.out.println(t1);
        System.out.println(t2);
    }
}
```





## OUTPUT:
<img width="1274" height="368" alt="image" src="https://github.com/user-attachments/assets/b9a2b318-b1f9-4941-b0bd-e00a8ba85b87" />



## RESULT:
Multithreading was successfully implemented. Multiple threads executed by setting the priority, demonstrating proper thread creation.



