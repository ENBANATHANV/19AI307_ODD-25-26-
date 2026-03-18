# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class that uses a constructor to initialize variables and overrides toString() method.

## AIM:
To write a Java program that uses a constructor to initialize a class’s variables and overrides the toString() method to display object details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class enba with private variables name and age.
4. Write a constructor enba(String s, int a) to initialize the variables.
5. Override the toString() method to return a formatted string of object details.
6. In the main() method:
Create a Scanner object to read input.
Read name and age from the user.
Create an object of class enba using the constructor.
Print the object (which calls the overridden toString() method).
7. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```
import java.util.*;
class enba{
    private String name;
    private int age;
    enba(String s , int a){
        this.name = s;
        this.age = a;
    }
    @Override
    public String toString(){
        return "Student{name='"+name+"', age="+age+"}";
    }
}
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner (System.in);
        String name = sc.nextLine();
        int age = sc.nextInt();
        enba obj = new enba(name , age);
        System.out.print(obj.toString());
        
    }
}
```






## OUTPUT:
<img width="763" height="315" alt="image" src="https://github.com/user-attachments/assets/09ae1c47-7901-4a78-8774-6424b2d8a88c" />



## RESULT:
Thus, the Java program using a constructor to initialize variables and overriding the toString() method was executed successfully. The object’s details were displayed in a user-friendly format.
