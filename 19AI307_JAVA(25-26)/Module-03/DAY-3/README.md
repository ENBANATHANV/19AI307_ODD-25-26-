# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create an abstract class Employee with method calculatePay(). Extend it to HourlyEmployee and SalariedEmploye

## AIM:
To write a Java program using an abstract class Employee with an abstract method calculatePay() and extend it to HourlyEmployee and SalariedEmployee to calculate pay for different types of employees.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an abstract class Employee with an abstract method calculatePay().
4. Create a class HourlyEmployee extending Employee:
Declare fields hours and rate.
Create a constructor to initialize these fields.
Override calculatePay() to return hours * rate.
5. Create a class SalariedEmployee extending Employee:
Declare a field value (salary).
Create a constructor to initialize value.
Override calculatePay() to return value.
6. In the main() method:
Create a Scanner object to read input.
Read an integer val to choose employee type (1 for hourly, else salaried).
For hourly employee: read hours and rate, create object, and call calculatePay().
For salaried employee: read salary, create object, and call calculatePay().
Display the calculated pay.
7. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: ENBANATHAN V 
RegisterNumber: 212224220027 
*/
```

## SOURCE CODE:
```
import java.util.*;
abstract class Employee{
    abstract double calculatePay();
    
}
class HourlyEmployee extends Employee{
    private int hours;
    private double rate;
    
   public HourlyEmployee(int a , double b){
        this.hours = a;
        this.rate = b;
    }
    @Override
    double calculatePay(){
        return hours*rate;
    }
}
class SalariedEmployee extends Employee{
    private double value;
    public SalariedEmployee(double a){
        this.value= a;
    }
    @Override
    double calculatePay(){
        return value;
    }
}
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner (System.in);
        int val = sc.nextInt();
        if(val==1)
        {
            int hour = sc.nextInt();
            double rate = sc.nextDouble();
            HourlyEmployee obj = new HourlyEmployee(hour,rate);
            System.out.print(obj.calculatePay());
        }
        else
        {
           double salary = sc.nextDouble();
           SalariedEmployee obi = new SalariedEmployee(salary);
           System.out.println(obi.calculatePay());
        }
    }
}
```






## OUTPUT:
<img width="412" height="279" alt="image" src="https://github.com/user-attachments/assets/6742e8ff-7a54-4d42-9d2b-8d15a1446201" />



## RESULT:
Thus, the Java program using an abstract class Employee and method overriding for HourlyEmployee and SalariedEmployee was executed successfully. The program calculates and displays pay based on employee type.
