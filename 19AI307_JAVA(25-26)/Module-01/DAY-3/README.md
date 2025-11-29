# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to check whether a number is Palindrome number. 

## AIM:
To write a Java program to check whether a number is Palindrome number. 

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Get the input from the user.
4.	INITIALIZE variable temp = num (to preserve the original number for later comparison) and sum = 0.
5.	ITERATE using a while loop as long as temp > 0 
6.	Calculate the remainder rem using temp % 10 (extract the last digit).
7.	Update sum using the formula sum * 10 + rem (build the reversed number).
8.	Update temp by dividing it by 10 (temp = temp / 10).
9.	COMPARE if the original number num is equal to the reversed number sum.
10.	IF the condition is true, DISPLAY "num is a Palindrome."
11.	ELSE, DISPLAY "num is not a Palindrome."
12.	STOP the program execution.





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:

```
import java.util.*;

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        
        int num = sc.nextInt();
        int temp = num, sum = 0;
        while(temp > 0){
            int rem = temp % 10;
            sum = sum * 10 + rem;
            temp /= 10;
        }
        if (num == sum){
            System.out.println(num +" is a Palindrome.");
        }else {
            System.out.println(num+" is not a Palindrome.");
        }
    }
}
```





## OUTPUT:
<img width="1284" height="358" alt="image" src="https://github.com/user-attachments/assets/42e7b61c-7471-47ea-8118-eff6980be167" />



## RESULT:
The Java program successfully implemented palindrome calculation using a for loop, producing correct outputs for all tested input values as per palindrome definitions.



