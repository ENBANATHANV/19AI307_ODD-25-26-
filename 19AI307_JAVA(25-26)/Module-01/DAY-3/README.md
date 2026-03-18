# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program that prompts the user to enter a non-negative integer and then calculates and displays the factorial of the given number.
Use a for loop to perform the calculation.
Make sure to handle the case when the user enters 0.
Display the result in a clear and user-friendly way.

## AIM:
To write a Java program to calculate the factorial of a non-negative integer using a for loop.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read input from the user.
4. Prompt the user to enter a non-negative integer.
5. Read the input number.
6. Initialize a variable fact = 1.
7. Check if the number is 0:
8. If yes, factorial is 1.
9. Otherwise, use a for loop from 1 to n:
10. Multiply fact with each number in the loop.
11. Display the factorial result in a clear format.
12. Stop the program.






## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner (System.in);
        int value = sc.nextInt();
        int count=1;
        for(int i=1;i<=value;i++)
        {
            count*=i;
        }
        System.out.print("Factorial of "+value+" is: "+count);
    }
}
```






## OUTPUT:
<img width="682" height="180" alt="image" src="https://github.com/user-attachments/assets/9e9817eb-f17b-4cb2-ae4c-e912c57929c2" />



## RESULT:
Thus, the Java program to calculate the factorial of a non-negative integer using a for loop was executed successfully, and the result was displayed.
