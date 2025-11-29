# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
At an international airport, only one Radar Control Tower exists. This tower is responsible for handling all flight communications regardless of how many flights are coming in. Each incoming flight must contact this tower to register its approach.
To ensure safety and consistency, all flights must communicate with the same instance of the tower. If multiple towers are created, it may lead to inconsistent instructions — a huge risk in aviation.
Your task is to simulate this system using the Singleton pattern.

## AIM:
To implement the Singleton Design Pattern in Java to simulate a Radar Control Tower system where only one instance manages all flight registrations.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. DEFINE a class RadarControlTower.
4. DECLARE a private static variable instance of type RadarControlTower (initially null).
5. DECLARE an integer variable flightCount initialized to 0.
6. DEFINE a private constructor RadarControlTower() to restrict object creation from outside the class.
7. DEFINE a public static method getInstance():
      IF instance is null, create a new object of RadarControlTower.
      RETURN the instance.
8. DEFINE a method registerFlight(flightName):
     Increment flightCount.
     Return the current flightCount.
9. IN MAIN METHOD:
     READ integer n (number of flights) from the user.
     ITERATE n times using a loop:
     READ the flightName.
     CALL RadarControlTower.getInstance() to get the single object reference.
      CALL registerFlight(flightName) using that reference.
      DISPLAY the flight name and the total count.
10. STOP the program.





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:

```
import java.util.*;

class RadarControlTower {
    private static RadarControlTower instance;  // Singleton instance
    private int flightCount;                    // To track number of registered flights

    // Private constructor to prevent creating multiple towers
    private RadarControlTower() {
        flightCount = 0;
    }

    // Public method to get the single instance of the tower
    public static RadarControlTower getInstance() {
        if (instance == null) {
            instance = new RadarControlTower();
        }
        return instance;
    }

    // Method to register a flight and increment the count
    public int registerFlight(String flightName) {
        flightCount++;
        return flightCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            String flight = sc.nextLine();
            RadarControlTower tower = RadarControlTower.getInstance();
            int total = tower.registerFlight(flight);
            System.out.println(flight + " registered with Radar Control Tower. Total Flights: " + total);
        }
    }
}

```





## OUTPUT:
<img width="1221" height="384" alt="image" src="https://github.com/user-attachments/assets/f86e04ef-2e1d-48de-b147-4a5fa15be656" />



## RESULT:
Thus, the Java program to simulate a Radar Control Tower using the Singleton Design Pattern was executed successfully and the output was verified.


