# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:
area(int side) for square
area(int length, int breadth) for rectangle
area(double radius) for circle

## AIM:
To write a Java program to calculate the area of different shapes (square, rectangle, circle) using method overloading.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class AreaCalculator.
4. Overload the area() method for different shapes:
5. area(int side) → calculates area of a square.
6. area(int length, int breadth) → calculates area of a rectangle.
7. area(double radius) → calculates area of a circle.
8. In the main() method:
9. Create a Scanner object.
10. Read required inputs: side, length, breadth, radius.
11. Create an object of AreaCalculator.
12. Call the overloaded area() methods and display the results.
13. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027  
*/
```

## SOURCE CODE:
```
import java.util.*;
class AreaCalculator {
    int area(int side){
        return side*side;
    }
    int area(int length, int breadth){
        return length*breadth;
    }
    double area(double radius){
        return Math.PI*radius*radius;
    }
}
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner (System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();
        double d = sc.nextDouble();
        AreaCalculator obj = new AreaCalculator();
        System.out.println("Area of square: "+obj.area(a));
        System.out.println("Area of rectangle: "+obj.area(b,c));
        System.out.println("Area of circle: "+obj.area(d));
    }
}
```






## OUTPUT:
<img width="866" height="395" alt="image" src="https://github.com/user-attachments/assets/df045e5a-1a0e-4bef-b716-8bbd955af337" />



## RESULT:
Thus, the Java program to calculate the area of square, rectangle, and circle using method overloading was executed successfully.
