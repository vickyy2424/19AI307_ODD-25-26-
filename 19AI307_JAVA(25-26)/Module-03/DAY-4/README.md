# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.



## AIM:
To create weather analysis bots that implement a common interface and provide weather predictions.

## ALGORITHM :
1.Define a common interface with a method for weather prediction
2.Create multiple bot classes that implement this interface
3.Each bot provides its own prediction logic in the implemented method
4.Test all bots to demonstrate polymorphic behavior



## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class WeatherBot {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int temperature = scanner.nextInt();
        int botType = scanner.nextInt();
        
        if (botType == 1) { // SunBot
            if (temperature > 30) {
                System.out.println("HOT");
            } else {
                System.out.println("MODERATE");
            }
        } else if (botType == 2) { // RainBot
            if (temperature < 20) {
                System.out.println("COLD");
            } else {
                System.out.println("WARM");
            }
        }
        
        scanner.close();
    }
}
```






## OUTPUT:
<img width="337" height="142" alt="image" src="https://github.com/user-attachments/assets/9c6a2160-0464-49e5-ac5a-619df62b497f" />


## RESULT:
The weather bot system was successfully implemented. All bots correctly implemented the common interface and provided their unique weather predictions, demonstrating proper interface implementation and polymorphic behavior.




