# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Write a Java program to reverse a string entered by the user.

Input:
A single line of text (a string) entered by the user via console.

Output:
The reversed string.

## AIM:
To write a Java program that takes a string as input from the user and displays the reversed string.

## ALGORITHM :
1.	Start the program.
2. Create a Scanner object to read input.
3. Prompt the user and read a string using nextLine().
4. Initialize an empty string variable to store the reversed result.
5. Use a for loop from the last index (length - 1) to 0.
6. In each iteration, append the current character to the reversed string.
7. After the loop, display the reversed string.
8. Stop the program.




## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027
*/
```

## Sourcecode.java:

```
import java.util.*;
public class vijay{
    public static void main(String[] args){
        Scanner sc=new Scanner (System.in);
        String a = sc.nextLine();
        int length=a.length()-1;
        for (int i=length;i>=0;i--)
        {
            System.out.print(a.charAt(i));
        }
    }
}
```



## OUTPUT:
<img width="448" height="212" alt="image" src="https://github.com/user-attachments/assets/d1ecf438-f658-4225-91c3-8a43c1a010ec" />



## RESULT:
Thus, the Java program to reverse a string entered by the user was executed successfully, and the reversed string was displayed.
