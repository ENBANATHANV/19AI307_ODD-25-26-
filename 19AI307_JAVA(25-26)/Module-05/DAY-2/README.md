# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.



## AIM:
To write a Java program that accepts user input, stores multiple Student objects in an ArrayList, serializes the collection into a file, and then deserializes it to display the stored data.
## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a class Student that implements Serializable.
4. Declare data members: id, name, and marks.
5. Define a constructor and override toString() method.
6. In the main class, create a Scanner object for user input.
7. Read the number of students n.
8. Use a loop to input student details (id, name, marks).
9. Store each object in an ArrayList<Student>.
Call serializeStudents() method:
Create ObjectOutputStream.
10. Write the list into a file using writeObject().
Call deserializeStudents() method:
Create ObjectInputStream.
11. Read the list from the file using readObject().
12. Display the deserialized student details.
13. Close the scanner.
14. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027 
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

// Student class must implement Serializable
class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    // Serialize list of students
    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    // Deserialize list of students
    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = sc.nextInt();
        sc.nextLine(); // consume newline
        for(int i=0;i<n;i++){
            int a = sc.nextInt();
            sc.nextLine();
            String b =sc.nextLine();
            double c = sc.nextDouble();
            students.add(new Student(a,b,c));
        }
        String name ="students.dat";
        serializeStudents(students, name);

// Deserialize
         List<Student> deserializedStudents = deserializeStudents(name); 
        
        // Write your code here

        // Display deserialized data
        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        sc.close();
    }
}

```






## OUTPUT:
<img width="1171" height="448" alt="image" src="https://github.com/user-attachments/assets/1a484d42-4a8b-49f8-bc34-105355e44329" />



## RESULT:
The program successfully demonstrates serialization and deserialization in Java using user input. Multiple Student objects are stored in a file and later retrieved correctly, preserving the data structure and values.
