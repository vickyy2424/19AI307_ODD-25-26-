# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to create a base class Vehicle with methods startEngine() and stopEngine(). Create two subclasses: Car and Motorcycle. Override the startEngine() and stopEngine() methods in each subclass to start and stop the engines differently.

## AIM:
To write a Java program to implement method overriding and demonstrate runtime polymorphism using a Vehicle class hierarchy.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	DEFINE a base class Vehicle with methods startEngine() and stopEngine() that print generic messages.
4.	DEFINE a subclass Car that extends Vehicle:
    OVERRIDE startEngine() to print "Car engine started with key ignition."
    OVERRIDE stopEngine() to print "Car engine stopped with key ignition."
5. DEFINE a subclass Motorcycle that extends Vehicle:
    OVERRIDE startEngine() to print "Motorcycle engine started with kick start."
    OVERRIDE stopEngine() to print "Motorcycle engine stopped using engine kill switch."
6. IN MAIN METHOD:
    CREATE a Scanner object to read input.
    READ the string vehicleType from the user.
    DECLARE a reference variable of type Vehicle. 
7. CHECK vehicleType using a switch statement:
    CASE "car": Instantiate vehicle = new Car().
    CASE "motorcycle": Instantiate vehicle = new Motorcycle().
    DEFAULT: Print "Invalid vehicle type" and terminate.
8. CALL vehicle.startEngine() and vehicle.stopEngine(). (The JVM determines which method to run based on the object type, not the reference type).
9. STOP the program.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

// Base class
class Vehicle {
    void startEngine() {
        System.out.println("Vehicle engine started.");
    }

    void stopEngine() {
        System.out.println("Vehicle engine stopped.");
    }
}

// Subclass Car
class Car extends Vehicle {
    @Override
    void startEngine() {
        System.out.println("Car engine started with key ignition.");
    }

    @Override
    void stopEngine() {
        System.out.println("Car engine stopped with key ignition.");
    }
}

// Subclass Motorcycle
class Motorcycle extends Vehicle {
    @Override
    void startEngine() {
        System.out.println("Motorcycle engine started with kick start.");
    }

    @Override
    void stopEngine() {
        System.out.println("Motorcycle engine stopped using engine kill switch.");
    }
}

// Main class
public class VehicleDemo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        String vehicleType = scanner.nextLine().toLowerCase();

        Vehicle vehicle;

        switch (vehicleType) {
            case "car":
                vehicle = new Car();
                break;
            case "motorcycle":
                vehicle = new Motorcycle();
                break;
            default:
                System.out.println("Invalid vehicle type selected.");
                scanner.close();
                return;
        }

        vehicle.startEngine();
        vehicle.stopEngine();

        scanner.close();
    }
}

```






## OUTPUT:
<img width="1267" height="372" alt="image" src="https://github.com/user-attachments/assets/aaa41f10-b112-4db8-a364-be58ec369d90" />

## RESULT: 
Thus, the Java program to demonstrate method overriding and runtime polymorphism using the Vehicle class hierarchy was executed successfully and the output was verified.


## RESULT:



