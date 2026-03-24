# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to write multiple lines to a file using FileWriter.



## AIM:
To write a Java program that accepts multiple lines of input from the user and writes them into a file using FileWriter.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read user input.
4. Create a file using the File class.
5. Create a FileWriter object to write into the file.
6. Use a loop to continuously accept input from the user.
7. If the user enters "exit", terminate the loop.
8. Write each input line into the file followed by a newline character.
9. Close the FileWriter to save the data.
10. Display a success message.
11. Handle any IOException if it occurs.
12. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: ENBANATHAN V
RegisterNumber:  212224220027
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.io.IOException;
import java.util.*;
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        try{
            File obj = new File("multilines.txt");
            obj.createNewFile();
            FileWriter obi = new FileWriter(obj);
            while(true){
                String a = sc.nextLine();
                if(a.equals("exit")) break;
                obi.write(a+"\n");
                
            }
            obi.close();
            System.out.println("File written successfully to "+obj.getName());
        }
        catch(IOException e){
            System.out.println("Failed");
        }
    }
}
```






## OUTPUT:

<img width="1076" height="199" alt="image" src="https://github.com/user-attachments/assets/eaa9beea-9e35-40a4-8d5f-0a51c2a890e1" />


## RESULT:
The program successfully writes multiple lines entered by the user into a file. The input continues until the user types "exit", and all entered lines are stored correctly in the file.
