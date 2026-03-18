# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".


## AIM:
To write a Java program to create a class Calculator with a non-static add method and a static info method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Calculator.
4. Define a non-static method add(int a, int b) that returns the sum of two numbers.
5. Define a static method info() that prints "Calculator is ready".
6. In the main() method:
7. Create a Scanner object to read two integers from the user.
8. Call the static method Calculator.info().
9. Create an object of Calculator class.
10. Call the non-static method add() using the object and display the result.
11. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027  
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Calculator {
   int add(int a, int b){
       return a+b;
   }
   static void info(){
       System.out.println("Calculator is ready");
   }
}

class prog {
    public static void main(String[] args) {
         Scanner sc = new Scanner (System.in);
         int a = sc.nextInt();
         int b = sc.nextInt();
         Calculator.info();
         Calculator obj = new Calculator();
         System.out.println("Sum: "+obj.add(a,b));
    }
}
```






## OUTPUT:
<img width="571" height="317" alt="image" src="https://github.com/user-attachments/assets/50fe39c4-2aa5-4f06-8959-38db2cbbd0f1" />



## RESULT:
Thus, the Java program to demonstrate a class with a static and non-static method was executed successfully. It displayed that the calculator is ready and printed the sum of two numbers.
