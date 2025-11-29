# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.


## AIM:
To write characters to a file using FileWriter class in Java.


## ALGORITHM :
1.Import necessary IO classes
2.Create FileWriter object with target filename
3.Use write() method to write character data to file
4.Close FileWriter to release resources
5.Verify file creation and content





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class WriteFileUsingFileWriter {
    public static void main(String[] args) {
    //write your code here
    try{
        FileWriter writer=new FileWriter("sample.txt");
        writer.write("welcome");
        writer.close();
        System.out.println("File written successfully.");
        
    }catch(IOException e)
    {
        System.out.println("An error occurred: " + e.getMessage());
    }
    
    
    
    }
}
```






## OUTPUT:
<img width="708" height="321" alt="image" src="https://github.com/user-attachments/assets/53553cc8-59d0-44d6-9f98-2f171be828b8" />


## RESULT:
The program successfully wrote character data to a file using FileWriter. The file was created with specified content and proper resource management was demonstrated through correct stream closing.




