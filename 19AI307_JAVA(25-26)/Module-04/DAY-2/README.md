# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a large office, multiple departments send print jobs to a shared central printer. To manage load and prevent collision, a Print Spooler Manager handles all job submissions.
The IT team insists that there should be only one spooler manager instance in the entire system. Regardless of how many jobs or departments exist, all jobs must pass through this one manager.
Your task is to simulate a singleton print job queue. Each print job submitted increases the queue count.

## AIM:
To implement a singleton Print Spooler Manager that manages all print jobs in a system, ensuring only one instance exists and maintains a count of submitted jobs.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.Create a class PrintSpoolerManager.
Declare a private static instance of the class.
Create a private constructor to prevent external instantiation.
Provide a public static method getInstance() to return the single instance.
Maintain a count variable to track print jobs.
Implement submitJob(String department) to increase the count and return it.
4. In the main() method:
Read the number of print jobs n from the user.
For each job:
Read the department name.
Get the singleton instance of PrintSpoolerManager.
Submit the job and display the total jobs in the queue.
5. Stop the program.	





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: ENBANATHAN V 
RegisterNumber: 212224220027  
*/
```

## SOURCE CODE:
```
import java.util.*;

class PrintSpoolerManager {
    private static  PrintSpoolerManager a;
    private int count=0;

    public static PrintSpoolerManager getInstance() {
          if(a==null){
              a = new PrintSpoolerManager();
          }
          return a;
     }

    public int submitJob(String department) {
      count++;
      return count;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String dept = sc.nextLine();
            PrintSpoolerManager spooler = PrintSpoolerManager.getInstance();
            int total = spooler.submitJob(dept);
            System.out.println(dept + " submitted a print job. Total Jobs in Queue: " + total);
        }
    }
}

```






## OUTPUT:

<img width="1193" height="443" alt="image" src="https://github.com/user-attachments/assets/c3e62654-7cef-4390-aa3f-5f89474df705" />


## RESULT:
The program successfully demonstrates the singleton pattern. All print jobs from multiple departments are handled by a single instance of the PrintSpoolerManager, and the total queue count increases correctly.
