# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the index of a given element in an array

## AIM:
To write a Java program to find the index of a given element in an array

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Get the length of the array from the user.
4.	Initialize an array of length n and get the inputs.
5.	Get the target from the user.
6.	If the element exist in the array return true else false.
7.	Stop the program. 





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
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
        int n = sc.nextInt();
        int[] arr = new int[n];
        
        for(int i = 0; i < n; i++){
            arr[i] = sc.nextInt();
        }
        boolean found = false;
        int element = sc.nextInt();
        
        for(int i = 0; i < n; i++){
            if (arr[i] == element){
                System.out.print(i);
                found = true;
            }
        }
        if (!found){
            System.out.println("Element not found");
        }
    }
}
```





## OUTPUT:
<img width="1229" height="613" alt="image" src="https://github.com/user-attachments/assets/5f3cdda8-360d-4b5c-82d9-1aa5f8dc20c8" />



## RESULT:
The program to find the existence of an element in an array is written and all the test casses passes successfully. 


