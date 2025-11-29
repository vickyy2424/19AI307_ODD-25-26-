# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.


## AIM:
To serialize an ArrayList of Student objects into a file using Java serialization.


## ALGORITHM :
1.Create Student class implementing Serializable interface
2.Create ArrayList of Student objects
3.Use ObjectOutputStream to serialize collection to file
4.Write ArrayList object to file using writeObject() method
5.Close resources and verify file creation


## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.ArrayList;
import java.util.Scanner;

class Student implements Serializable {
    private static final long serialVersionUID = 1L;
    private int id;
    private String name;
    private double marks;
    
    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }
    
    // Getters
    public int getId() { return id; }
    public String getName() { return name; }
    public double getMarks() { return marks; }
    
    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerialization {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        ArrayList<Student> students = new ArrayList<>();
        
        // Read number of students
        int n = Integer.parseInt(scanner.nextLine());
        
        // Read student details
        for (int i = 0; i < n; i++) {
            int id = Integer.parseInt(scanner.nextLine());
            String name = scanner.nextLine();
            double marks = Double.parseDouble(scanner.nextLine());
            
            students.add(new Student(id, name, marks));
        }
        
        String filename = "students.dat";
        
        // Serialize the collection
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(filename))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + filename);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
            return;
        }
        
        // Deserialize the collection
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(filename))) {
            @SuppressWarnings("unchecked")
            ArrayList<Student> deserializedStudents = (ArrayList<Student>) ois.readObject();
            
            System.out.println("Students deserialized successfully from: " + filename);
            System.out.println("\nDeserialized Students:");
            for (Student student : deserializedStudents) {
                System.out.println(student);
            }
            
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        
        scanner.close();
    }
}
```




## OUTPUT:
<img width="1176" height="473" alt="image" src="https://github.com/user-attachments/assets/76dab857-0fa0-4992-a9a6-381b098803b7" />


## RESULT:
The ArrayList of Student objects was successfully serialized to a file. The serialization process preserved the entire collection structure and object data, demonstrating proper Java object serialization.





