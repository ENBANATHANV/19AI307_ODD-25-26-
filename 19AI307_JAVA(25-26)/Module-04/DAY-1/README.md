# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
To write a Java program that reads two integers, divides the first by the second, and handles the case when division by zero occurs.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read integers.
4. Use a try block to:
Read two integers a and b.
Perform a / b and store the result.
Print the result.
5.Use a catch block for ArithmeticException:
Print an error message "Error: Division by zero".
6. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Vijayy{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        try{
            int a = sc.nextInt();
            int b = sc.nextInt();
            int c = a/b;
            System.out.print("Result: "+c);
        }
        catch(ArithmeticException e){
            System.out.print("Error: Division by zero");
        }
    }
}
```






## OUTPUT:
<img width="719" height="323" alt="image" src="https://github.com/user-attachments/assets/8a7b5b04-1167-416a-8bbe-86eac1b174b9" />



## RESULT:
The program successfully divides two integers and handles the case of division by zero using exception handling.
