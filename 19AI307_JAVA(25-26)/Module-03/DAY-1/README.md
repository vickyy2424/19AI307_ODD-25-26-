# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:
finalPrice = purchaseWeight * (goldRatePerGram - discount)
For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:
To write a Java program to implement inheritance and method overriding for calculating gold prices based on customer types (Regular and Premium).

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	DEFINE a base class Customer with attributes: customerId, name, purchaseWeight, goldRatePerGram.
4.	DEFINE methods in base class:
5.	getDiscountRate(): Returns 0 by default.
6.	calculateFinalPrice(): Calculates price using the formula: weight * (rate - (rate * discount/100)).
7.	DEFINE subclass RegularCustomer extending Customer:
      OVERRIDE getDiscountRate() to return 2.0.
8.	DEFINE subclass PremiumCustomer extending Customer:
      OVERRIDE getDiscountRate() to return 5.0.
11.	DEFINE calculateCashback(): Returns 1% of the final price.
12.	IN MAIN METHOD:
13.	READ inputs: customerType, id, name, weight, rate.
14.	CHECK customerType:
15.	IF "Regular": Create object of RegularCustomer.
    ELSE IF "Premium": Create object of PremiumCustomer.
    ELSE: Create object of base Customer.
16. CALL the display() method to show details, calculated price, and cashback (if applicable).
17. STOP the program.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
import java.text.DecimalFormat;

class Order {
    String orderId;
    String customerName;
    double totalAmount;
    double deliveryCharge;

    public Order(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        this.orderId = orderId;
        this.customerName = customerName;
        this.totalAmount = totalAmount;
        this.deliveryCharge = deliveryCharge;
    }

    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    void display(String userType) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: " + userType);
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
    }
}

// Continue your code here
class NormalUser extends Order {
    NormalUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }

    double calculateFinalAmount() {
        return totalAmount + deliveryCharge;
    }

    void display(String userType) {
        super.display("Normal");
    }
}

class PrimeUser extends Order {
    PrimeUser(String orderId, String customerName, double totalAmount, double deliveryCharge) {
        super(orderId, customerName, totalAmount, deliveryCharge);
    }

    double calculateFinalAmount() {
        return totalAmount + (deliveryCharge * 0.5);
    }

    void display(String userType) {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Order ID: " + orderId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("User Type: Prime");
        System.out.println("Total Amount: " + totalAmount);
        System.out.println("Delivery Charge: " + deliveryCharge);
        System.out.println("Final Amount: " + df.format(calculateFinalAmount()));
    }
}

public class FoodDeliveryApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        
            String type = sc.next();
          
            String orderId = sc.next();
            
            String name = sc.next();
            
            double total = sc.nextDouble();
            
            double delivery = sc.nextDouble();

            Order order;
            if (type.equalsIgnoreCase("Prime"))
                order = new PrimeUser(orderId, name, total, delivery);
            else
                order = new NormalUser(orderId, name, total, delivery);

            order.display(type);
       

        sc.close();
    }
}

```





## OUTPUT:
<img width="1272" height="745" alt="image" src="https://github.com/user-attachments/assets/47d7884c-4f1e-427c-b2a1-9c45f8eaeb09" />



## RESULT:
Thus, the Java program to track gold rates and calculate prices for different customer types using inheritance and method overriding was executed successfully and the output was verified.



