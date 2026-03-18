# Ex.No:2(B) METHODS

## QUESTION:
Write a class with one static method and one non-static method. Call both from the main() method.
When staticMethod() is called, it should print  "I am static".
When nonStaticMethod() is called, it should print  "I am non-static"

## AIM:
To write a Java program with one static method and one non-static method, and call both from the main() method.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Vijay.
4. Define a static method staticMethod() that prints "I am static".
5. Define a non-static method nonStaticMethod() that prints "I am non-static".
6. In the main() method:
   Call the static method directly.
   Create an object of the class.
   Call the non-static method using the object.
7. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Vijay{
    static void staticMethod(){
        System.out.println("I am static");
    }
    void nonStaticMethod(){
        System.out.print("I am non-static");
    }
    public static void main(String[] args){
        staticMethod();
        Vijay obj = new Vijay();
        obj.nonStaticMethod();
        
    }
}
```






## OUTPUT:
<img width="495" height="186" alt="image" src="https://github.com/user-attachments/assets/537d4936-10ee-4a19-82dc-ce726f45885b" />



## RESULT:
Thus, the Java program with one static and one non-static method was executed successfully, and the output displayed the messages correctly.
