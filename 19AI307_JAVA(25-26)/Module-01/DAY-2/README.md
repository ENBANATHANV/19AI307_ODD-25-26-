# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A pirate ship has a code lock that only opens if:
     The input code is even, and
     If it is less than 100, say "Weak Code".
     If it is between 100 and 999, say "Strong Code".
If the code is odd, deny access -"Access Denied".

## AIM:
To write a Java program to check whether the entered code is valid for a pirate ship lock based on given conditions.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to take input from the user.
4. Prompt the user to enter the code.
5. Read the input number.
6. Check if the number is even (code % 2 == 0).
   If the number is even:
   If it is less than 100, display "Weak Code".
7.Else if it is between 100 and 999, display "Strong Code".
8.If the number is odd, display "Access Denied".
9.Stop the program.





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
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
        int value=sc.nextInt();
       if (value%2==0)
       {
           if (value<100)
           {
             System.out.print("Weak Code");  
           }
           else if (value>100 && value<999)
           {
                System.out.print("Strong Code");
           }
           else
           {
               System.out.print("Access Denied");
           }
           
       }
       else
       {
           System.out.print("Access Denied");
       }
    }
}
```






## OUTPUT:
<img width="487" height="296" alt="image" src="https://github.com/user-attachments/assets/e9f67343-1f16-41de-adf0-2579f93a256a" />


## RESULT:
Thus, the Java program to check the pirate ship code lock conditions was executed successfully, and the appropriate message was displayed based on the input.
