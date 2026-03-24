# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## AIM:
To demonstrate chaining of input streams in Java using BufferedReader and InputStreamReader to read user input (name and age) from the keyboard and display it.

## ALGORITHM :
1. Start the program.
2. Import the necessary packages java.io.*.
3. Create an InputStreamReader object to read bytes from System.in.
4. Create a BufferedReader object and chain it with InputStreamReader.
5. Prompt the user to enter their name.
6. Read the name using readLine() method.
7. Prompt the user to enter their age.
8. Read the age using readLine() method.
9. Convert the age from string to integer using Integer.parseInt().
10. Display the name and age.
11. Handle possible IOException using try-catch block.
12. Stop the program.




## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) {
        // Chaining: System.in -> InputStreamReader -> BufferedReader
        try{
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
             String name = br.readLine();
             int age = Integer.parseInt(br.readLine());
             System.out.println("--- User Details ---");
             System.out.println("Name: "+name);
             System.out.println("Age: "+age);
            
        }
        catch(IOException e){
            System.out.println(e);
        }

       //Write your code here
    }
}

```






## OUTPUT:
<img width="561" height="475" alt="image" src="https://github.com/user-attachments/assets/fb9dcd41-f4a5-4397-a042-e4847a884e13" />



## RESULT:

The program successfully demonstrates chaining of streams using BufferedReader and InputStreamReader to read input from the user and displays the entered name and age correctly.
