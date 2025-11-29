# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:


## AIM:


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Read input n → number of deposits.
4. Read n deposit amounts into an array.
5. Create a BankAccount object with balance = 0.
6. Create n threads, each depositing one amount into the same account.
7. Start all threads.
8. Wait for all threads to finish using join().
9. Print the final balance.
10. Stop the program. 




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Vigneshwaran S
RegisterNumber:  212224060301
*/
```

## SOURCE CODE:
```
import java.util.*;

class BankAccount {
    private int balance = 0;

    public synchronized void deposit(int amount) {
        balance += amount;
    }

    public int getBalance() {
        return balance;
    }
}

public class BankDepositSimulation {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        
        int n = sc.nextInt();  
        int[] amounts = new int[n];

        for (int i = 0; i < n; i++) {
            amounts[i] = sc.nextInt();
        }

        BankAccount account = new BankAccount();
        Thread[] threads = new Thread[n];

        // Create threads
        for (int i = 0; i < n; i++) {
            int amount = amounts[i];
            threads[i] = new Thread(() -> account.deposit(amount));
        }

        // Start all threads
        for (Thread t : threads) {
            t.start();
        }

        // Wait for all to finish
        for (Thread t : threads) {
            t.join();
        }


        System.out.println("Final Balance: " + account.getBalance());
    }
}

```






## OUTPUT:
<img width="1274" height="585" alt="image" src="https://github.com/user-attachments/assets/7413bd0e-6e60-488e-b9db-22fb672b52dd" />


## RESULT:
Thus, the final balance is equal to the sum of all deposit amounts, because each thread safely updates the shared balance using the synchronized deposit method.


