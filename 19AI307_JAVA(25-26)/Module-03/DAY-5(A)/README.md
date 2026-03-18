# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.

## AIM:
To write a Java program that creates an inner class and accesses it from the outer class.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an outer class outer.
4. Inside the outer class, create an inner class inner.
5. In the inner class, define a method display(String a) to print a message including the input string.
6. In the main() method:
Create a Scanner object to read input.
Read a string from the user.
Create an object of the outer class.
Create an object of the inner class using the outer class object.
Call the display() method of the inner class object.
7. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027  
*/
```

## SOURCE CODE:
```
import java.util.*;
class outer{
    class inner{
        void display(String a)
        {
            System.out.print("Hello, "+a+"! This message is from the Inner Class.");
        }
    }
}
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner (System.in);
        String a = sc.next();
        outer out = new outer();
        outer.inner obj = out.new inner();
        obj.display(a);
    }
}
```






## OUTPUT:
<img width="1188" height="260" alt="image" src="https://github.com/user-attachments/assets/466a9238-6f84-4b0c-8a10-4a3c98e8e7ad" />



## RESULT:
Thus, the Java program successfully created an inner class and accessed its method from the outer class. The program displays a message using the inner class.
