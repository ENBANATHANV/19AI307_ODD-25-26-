# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.
Bot Types:
SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".
RainBot: Predicts "COLD" if temperature < 20, else "WARM".


## AIM:
To write a Java program that uses an interface vijay to implement two types of bots (SunBot and RainBot) that predict weather based on temperature.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface vijay with a method prediction(int a).
4. Create a class SunBot that implements vijay:
If temperature > 30 → print "HOT".
Else → print "MODERATE".
5. Create a class RainBot that implements vijay:
If temperature < 20 → print "COLD".
Else → print "WARM".
In the main() method:
6. Create a Scanner object.
Read two integers: value (temperature) and check (bot type: 1 → SunBot, else RainBot).
Declare a reference of type vijay.
Based on check, initialize the reference with SunBot or RainBot.
Call the prediction() method using the reference.
7. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: ENBANATHAN V 
RegisterNumber: 212224220027 
*/
```

## SOURCE CODE:
```
import java.util.*;
interface vijay{
    void prediction(int a);
}
class SunBot implements vijay{
    public void prediction(int b){
        if(b>30)
        {
            System.out.print("HOT");
        }
        else
        {
            System.out.print("MODERATE");
        }
    }
}
class RainBot implements vijay{
    public void prediction(int b){
        if(b<20)
        {
            System.out.print("COLD");
        }
        else
        {
            System.out.print("WARM");
        }
    }
}
public class enba{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        vijay p;
        int value = sc.nextInt();
        int check = sc.nextInt();
        if(check==1)
        {
            p = new SunBot();
        }
        else
        {
            p = new RainBot();
        }
        p.prediction(value);
    }
}
```






## OUTPUT:
<img width="347" height="162" alt="image" src="https://github.com/user-attachments/assets/9312cc65-8b8f-4625-9228-b5d4f1dc1bb9" />



## RESULT:
Thus, the Java program using an interface and polymorphism to implement SunBot and RainBot was executed successfully. The program predicted the weather based on temperature.
