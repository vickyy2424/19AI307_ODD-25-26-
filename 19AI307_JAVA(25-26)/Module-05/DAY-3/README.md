# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of words in a file.


## AIM:
To write a program to count the number of words in a file.


## ALGORITHM :
1.Import java.io package
2.Calculate the number of words in the file.
3.Print the output. 
4.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:
```
import java.util.*;

public class WordCount {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String line = sc.nextLine();

        String[] words = line.trim().split("\\s+");

        int count = (line.trim().isEmpty()) ? 0 : words.length;

        System.out.println("Number of words in the file: " + count);
    }
}

```




## OUTPUT:
<img width="1226" height="380" alt="image" src="https://github.com/user-attachments/assets/1e60ed3e-1744-45a1-9209-7e5cbd17c4c9" />

## RESULT:
The program successfully created a to calculate the number of words in the file. 




