# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently.

## AIM:
To implement a composition relationship in Java where a Library contains multiple Book objects. Each Book is created within the Library, demonstrating that books cannot exist independently outside the library.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Library class that will hold a list of Book objects.
4.	Create a Book class with private attributes title and author and a method getDetails() to return book information.
5. Inside the Library class, implement:
A List<Book> to store books.
A method addBook(title, author) to create a Book object and add it to the list.
A method showBooks() to display all books in the library.
6. In the main method:
Create a Scanner object to read user input.
Create a Library object.
Read the number of books n to be added.
For i = 1 to n:
Read title and author from the user.
Call library.addBook(title, author) to add the book.
7. Call library.showBooks() to display the list of books.
8. Close the Scanner object to avoid memory leaks.
9. End the program.





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027
*/
```

## SOURCE CODE:

```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> book = new ArrayList<>();
    public void addBook(String title, String author) {
        Book books = new Book(title,author);
        book.add(books);
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for(Book a: book)
        {
            System.out.println("- "+a.getDetails());
        }
    }
}



```





## OUTPUT:
<img width="933" height="538" alt="image" src="https://github.com/user-attachments/assets/045d010d-fc02-48ad-8056-e0967cb87c08" />



## RESULT:
The program successfully demonstrates the composition relationship. All books are created and managed inside a single Library instance, and the list of books is displayed correctly.
