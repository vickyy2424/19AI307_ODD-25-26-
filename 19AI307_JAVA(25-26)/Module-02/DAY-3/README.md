# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	DEFINE class BankAccount with private variables and public getter/setter methods
4.	CREATE Scanner object to read user input
5.	READ String accNo and double bal from user
6.	CREATE object acc of class BankAccount
7.	INVOKE acc.setAccountNumber(accNo) to assign the private account number
8.	INVOKE acc.setBalance(bal) to assign the private balance
9.	CALL acc.getAccountNumber() to retrieve the data and DISPLAY the Account Number
10.	CALL acc.getBalance() to retrieve the data and DISPLAY the Balance
11.	STOP the program execution





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class BankAccount {
    // Private instance variables
    private String accountNumber;
    private double balance;

    // Getter and Setter for accountNumber
    public String getAccountNumber() {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }

    // Getter and Setter for balance
    public double getBalance() {
        return balance;
    }
    public void setBalance(double balance) {
        this.balance = balance;
    }
}

public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String accNo = sc.nextLine();
        double bal = sc.nextDouble();
        
        BankAccount acc = new BankAccount();
        acc.setAccountNumber(accNo);
        acc.setBalance(bal);
        System.out.println("Account Number: "+acc.getAccountNumber());
        System.out.println("Balance: "+acc.getBalance());
        
    }
}
```





## OUTPUT:

<img width="1229" height="465" alt="image" src="https://github.com/user-attachments/assets/9b45e3b4-c96b-42d7-80bd-15437f069983" />


## RESULT:

Hence a Java program to create a class called BankAccount with private instance variables accountNumber and balance and to provide public getter and setter methods to access and modify these variables was done successfully and passed all the test cases. 


