# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Synchronize deposit method in a BankAccount class, simulate deposits from multiple threads.

## AIM:
To implement a thread-safe bank account system in Java by synchronizing the deposit method, and to simulate multiple concurrent deposit operations using threads to ensure correct final balance.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create a class BankAccount
Initialize balance to 0
Define a synchronized method deposit(amount) to safely add money
Define getBalance() to return final balance
4. In the main class:
Read number of deposit operations n from user
Create a BankAccount object
Create an array of Thread objects of size n
5. For each thread:
Read deposit amount
Create a thread that calls deposit(amount)
Start the thread
6. Wait for all threads to finish using join()
7. Print the final account balance
8. End the program	





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

class BankAccount {
    private int balance = 0;  // Initial balance is 0

    // Synchronized method to safely deposit money
    public synchronized void deposit(int amount) {
        balance += amount;
    }

    // Method to get the final balance
    public int getBalance() {
        return balance;
    }
}

public class BankSimulation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read number of threads (deposit operations)
        int n = sc.nextInt();
        
        // Create a BankAccount object
        BankAccount account = new BankAccount();

        // Create and start threads for each deposit
        Thread[] threads = new Thread[n];
        for (int i = 0; i < n; i++) {
            int depositAmount = sc.nextInt();  // Read the deposit amount for this thread
            threads[i] = new Thread(() -> account.deposit(depositAmount));  // Create a new thread for deposit
            threads[i].start();  // Start the thread
        }

        // Wait for all threads to finish
        try {
            for (int i = 0; i < n; i++) {
                threads[i].join();  // Ensure each thread has completed
            }
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        // Print the final balance after all deposits
        System.out.println("Final Balance: " + account.getBalance());

        sc.close();
    }
}
```





## OUTPUT:
<img width="546" height="465" alt="image" src="https://github.com/user-attachments/assets/f21cef77-9600-4820-a854-748c4ccebce1" />



## RESULT:
The program performs concurrent deposits using multiple threads and ensures thread safety using a synchronized method.
