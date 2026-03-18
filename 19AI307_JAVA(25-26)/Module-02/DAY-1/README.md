# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To write a Java program to create a class Car with attributes brand, model, and year, create two objects, and display their details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Define a class Car with attributes brand, model, and year.
4. In the main method, create two objects of the Car class.
5. Assign values to the attributes of both objects
6. Print the details of both objects using System.out.println().
7. Stop the program.	





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027 
*/
```

## SOURCE CODE:
```
public class prog {
    public static class Car{
        String brand;
        String model;
        int year;
    }
    public static void main(String[] args) {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}

```






## OUTPUT:
<img width="590" height="185" alt="image" src="https://github.com/user-attachments/assets/71cea2d6-9dcb-4c0d-a619-26a2f20b5557" />



## RESULT:
Thus, the Java program to create a class Car, instantiate two objects, and display their details was executed successfully.
