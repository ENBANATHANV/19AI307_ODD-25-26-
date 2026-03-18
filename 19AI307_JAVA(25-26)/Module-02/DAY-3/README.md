# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Circle with a private instance variable radius. Provide public getter and setter methods to access and modify the radius variable. However, provide two methods called calculateArea() and calculatePerimeter() that return the calculated area and perimeter based on the current radius value. 

## AIM:
To write a Java program to create a class Circle with a private radius, provide getter and setter methods, and calculate the area and perimeter of the circle.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Circle with a private variable radius.
4. Provide a public getRadius() method to return the radius.
5. Provide a public setRadius(double radius) method to modify the radius.
6. Create a method calculateArea() that returns π * radius * radius.
7. Create a method calculatePerimeter() that returns 2 * π * radius.
8. In the main() method:
Create a Scanner object to read input.
Read the radius value from the user.
Create an object of Circle class.
Set the radius using the setter method.
Display the radius, area, and perimeter using getter and calculation methods.
9. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Circle {
   
    private double radius;

  
    public double getRadius() {
        return radius;
    }

   
    public void setRadius(double radius) {
        this.radius = radius;
    }

    
    public double calculateArea() {
        return Math.PI * radius * radius;
    }

   
    public double calculatePerimeter() {
        return 2 * Math.PI * radius;
    }
}
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner (System.in);
        double value = sc.nextDouble();
        Circle obj = new Circle();
        obj.setRadius(value);
        System.out.printf("Radius: %.2f\n",obj.getRadius());
        System.out.printf("Area: %.2f\n",obj.calculateArea());
        System.out.printf("Perimeter: %.2f",obj.calculatePerimeter());
    }
}
```






## OUTPUT:
<img width="597" height="299" alt="image" src="https://github.com/user-attachments/assets/6d918576-ab20-4f1e-aaaa-10a68736a924" />



## RESULT:
Thus, the Java program to create a class Circle with a private radius, along with getter, setter, and calculation methods, was executed successfully. The program displays the radius, area, and perimeter based on user input.
