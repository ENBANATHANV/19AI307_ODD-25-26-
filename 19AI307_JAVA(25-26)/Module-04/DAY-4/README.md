# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:
To implement the Abstract Factory design pattern where a UI toolkit can generate families of related objects (Button and Checkbox) for different themes (dark and light). Users choose a theme, and the program creates the corresponding UI components dynamically.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Define abstract interfaces:
Button with paint() method.
Checkbox with paint() method.
4. Create concrete classes for each theme:
LightButton, DarkButton implement Button.
LightCheckbox, DarkCheckbox implement Checkbox.
Each paint() method prints the type of component created.
5. Define an abstract factory interface UIfactory with methods:
Button get() → returns a Button.
Checkbox get1() → returns a Checkbox.
6. Create concrete factories:
Lighttheme implements UIfactory and returns LightButton and LightCheckbox.
Darktheme implements UIfactory and returns DarkButton and DarkCheckbox.
7. In main method:
Read the theme from the user.
Instantiate the corresponding factory (Lighttheme or Darktheme).
Use the factory to create a Button and a Checkbox.
Call paint() on both objects to display their type.
8. End the program.





## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027 
*/
```

## SOURCE CODE:
```
import java.util.*;
interface Button{
    void paint();
}
interface Checkbox{
    void paint();
}
class LightButton implements Button{
    public void paint(){
        System.out.println("Light Button created");
    }
}
class DarkButton implements Button{
    public void paint(){
        System.out.println("Dark Button created");
    }
}
class LightCheckbox implements Checkbox{
    public void paint(){
        System.out.println("Light Checkbox created");
    }
}
class DarkCheckbox implements Checkbox{
    public void paint(){
        System.out.println("Dark Checkbox created");
    }
}
interface UIfactory{
    Button get();
    Checkbox get1();
}
class Lighttheme implements UIfactory{
    public Button get() {
        return new LightButton();
    }
    public Checkbox get1() {
        return new LightCheckbox();
    }
}
class Darktheme implements UIfactory{
    public Button get() {
        return new DarkButton();
    }
    public Checkbox get1() {
        return new DarkCheckbox();
    }
}
public class Vijay{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        String a = sc.next().toLowerCase().trim();
        UIfactory obj;
        switch(a){
            case "dark":
                obj = new Darktheme();
                break;
            case "light":
                obj = new Lighttheme();
                break;
            default:
                System.out.println("Invalid theme");
                return;
        }
        Button obi = obj.get();
        Checkbox ob1 = obj.get1();
        obi.paint();
        ob1.paint();
    }
}
```






## OUTPUT:
<img width="595" height="229" alt="image" src="https://github.com/user-attachments/assets/d7845bc5-57b9-418e-b241-f27af2e88a13" />



## RESULT:
The program successfully demonstrates the Abstract Factory pattern. Based on the user-selected theme, corresponding Button and Checkbox objects are created, and their types are displayed correctly.
