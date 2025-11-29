# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Define a class Car with brand (String), color (String), and year (int). Create 2 different objects of Car  Assign values to attributes. Print the details of both cars. 

## AIM:
To create a Car class with attributes brand, color, and year, and display details of two objects of the class.

## ALGORITHM :
1.Define a class named Car.
2.Declare three attributes: brand, color, and year.
3.Create a constructor to initialize these attributes.
4.Create a method to display the car details.
5.In the main method, create two objects of the Car class.
6.Print the details of both objects.





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:
```
import java.util.*;
class Car {
    String brand;
    String color;
    int year;

    void printDetails() {
        System.out.println("Brand: "+brand);
        System.out.println("Color: "+color);
        System.out.println("Year: "+year);
        
    }
}

class prog {
    public static void main(String[] args) {
        // Your Code Here
        Scanner sc = new Scanner(System.in);
        Car c1 = new Car();
        c1.brand = sc.next();
        c1.color = sc.next();
        c1.year = sc.nextInt();
        
        Car c2 = new Car();
        c2.brand = sc.next();
        c2.color = sc.next();
        c2.year = sc.nextInt();
        
        c1.printDetails();
        c2.printDetails();
        sc.close();

    }
}
```






## OUTPUT:

<img width="1223" height="700" alt="image" src="https://github.com/user-attachments/assets/c7950b60-73e5-4e60-9a74-eec1b1a8011f" />



## RESULT:
The Car class was successfully implemented with attributes brand, color, and year. Two objects were created and their details were displayed correctly, confirming proper class functionality.





