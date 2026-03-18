# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To write a Java program to check whether a number is an Armstrong number using Math.pow() and the Integer wrapper class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number as a String from the user.
4. Convert the string to an Integer using Integer.valueOf().
5. Store the original number and initialize sum = 0.
6. Find the number of digits (digit = length of string).
7. Use a while loop:
Get the last digit using number % 10.
Add Math.pow(digit, number of digits) to sum.
Remove the last digit using number / 10.
8. Compare sum with the original number:
If equal → print “Armstrong number”.
Else → print “Not an Armstrong number”.
9. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027  
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String a = sc.next();
        Integer value = Integer.valueOf(a);
        
        int number = value;
        int sum=0;
        int digit = a.length();
        while(number>0)
        {
            int val = number%10;
            sum+=(int)Math.pow(val,digit);
            number=number/10;
        }
        if(sum==value)
        {
            System.out.print(value+" is an Armstrong number.");
        }
        else
        {
            System.out.print(value+" is not an Armstrong number.");
        }
    }
}
```






## OUTPUT:
<img width="805" height="254" alt="image" src="https://github.com/user-attachments/assets/60e88ad1-a229-424f-9568-4dad9880a7f9" />



## RESULT:
Thus, the Java program to check whether a number is an Armstrong number using Math.pow() and the Integer wrapper class was executed successfully
