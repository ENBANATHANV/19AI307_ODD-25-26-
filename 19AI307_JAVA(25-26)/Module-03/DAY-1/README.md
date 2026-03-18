# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Vehicle with fields brand (String) and speed (int). Create a subclass Car that inherits from Vehicle and adds a field fuelType (String).
Implement a method in Car called displayInfo() that prints the vehicle's brand, speed, and fuel type.

## AIM:
To write a Java program that creates a superclass Vehicle and a subclass Car which adds a fuelType field, and display all details using a method in the subclass.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a superclass Vehicle with fields brand (String) and speed (int).
4. Create a subclass Car that extends Vehicle and adds a field fuelType (String).
5. In Car, implement a method displayInfo() to print brand, speed, and fuelType.
6. In the main() method:
Create a Scanner object.
Create an object of Car.
Read the brand, speed, and fuelType from the user.
Call the displayInfo() method.
7. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027  
*/
```

## SOURCE CODE:
```
import java.util.*;
class Vehicle{
    String brand;
    int speed;
}
class Car extends Vehicle{
    String fuelType;
    void displayInfo(){
        System.out.println("Brand: "+brand);
        System.out.println("Speed: "+speed+" km/h");
        System.out.println("Fuel Type: "+fuelType);
    }
}
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        Car obj = new Car();
        obj.brand = sc.next();
        obj.speed = sc.nextInt();
        obj.fuelType = sc.next();
        obj.displayInfo();
    }
}
```






## OUTPUT:
<img width="728" height="396" alt="image" src="https://github.com/user-attachments/assets/825eebbd-687b-41b4-838a-f149694f4c28" />



## RESULT:
Thus, the Java program demonstrating inheritance by creating a Vehicle superclass and Car subclass was executed successfully. The program displayed the brand, speed, and fuel type of the car.
