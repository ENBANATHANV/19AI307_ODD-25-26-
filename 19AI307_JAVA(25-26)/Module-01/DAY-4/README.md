# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements

## AIM:
To write a Java program to find the average of array elements.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Scanner object for input.
4. Enter the number of elements (n).
5. Declare an array of size n.
6. Initialize sum = 0.
7. Use a loop to read array elements.
8. Add each element to sum.
9. Calculate average = sum / n.
10. Display the average.
11. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027 
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner (System.in);
        int a = sc.nextInt();
        int[] arr = new int[a];
        int sum=0;
        System.out.print("The average of elements is ");
        for (int i=0;i<a;i++)
        {
            arr[i]=sc.nextInt();
            sum+=arr[i];
        }
        double value = (double)sum/a;
        System.out.printf("%.2f",value);
    }
}
```






## OUTPUT:
<img width="784" height="485" alt="image" src="https://github.com/user-attachments/assets/622c299e-317a-4a0e-a374-5a9c5f38c4bf" />



## RESULT:
Thus, the Java program to find the average of array elements was executed successfully, and the average was displayed.
