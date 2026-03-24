# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.



## AIM:
To write a Java program to determine and display the name and priority of the current thread.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object to read user input.
4. Read the thread name from the user.
5. Create a Thread object.
6. Set the thread name using setName().
7. Set the thread priority using setPriority().
8. Retrieve and display the thread priority using getPriority().
9. Retrieve and display the thread name using getName().
10. Print the thread object.
11. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: ENBANATHAN V
RegisterNumber:  212224220027
*/
```

## SOURCE CODE:

```
import java.util.*;
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        
        Thread a1 = new Thread();
        a1.setName(name);
        a1.setPriority(5);
        System.out.println("Priority of Thread: "+a1.getPriority());
        System.out.println("Name of Thread: "+a1.getName());
        System.out.println(a1);
    }
}
```





## OUTPUT:
<img width="715" height="206" alt="image" src="https://github.com/user-attachments/assets/9767ce4f-d56b-4d27-9a01-f88cf34d4e33" />



## RESULT:
The program successfully creates a thread, assigns a user-defined name and a priority, and displays the thread’s name and priority correctly.
