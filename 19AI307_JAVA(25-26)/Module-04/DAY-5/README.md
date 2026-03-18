# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create a class Note that stores a note content. Allow saving multiple versions and restoring a previous one. (Memento Pattern)



## AIM:
To implement the Memento Design Pattern to allow a Note object to save multiple versions of its content and restore any previous version.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create a Note class with:
content (the current note).
save() method → returns a NoteMemento object storing the current content.
restore(NoteMemento) → restores content from a saved memento.
show() → prints the content.
4. Create a NoteMemento class to store a snapshot of note content.
5. Create a NoteHistory class:
Stores a list of NoteMemento objects.
store(NoteMemento) → saves a version.
get(int index) → retrieves a previous version.
6. In main method:
Read number of versions a.
For each version:
Read the note content.
Save it into NoteHistory.
Read an index b to restore.
Restore the note to version b and display it.
7. End the program.





## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: ENBANATHAN V
RegisterNumber: 212224220027
*/
```

## SOURCE CODE:
```
import java.util.*;

class Note {
    private String content;
    public void setName(String name){
        this.content=name;
    }
    public NoteMemento save(){
        return new NoteMemento (content);
    }
    public void restore(NoteMemento m){
        content = m.getName();
    }
    public void show(){
        System.out.println(content);
    }
    // TODO: Setter and Getter for content
}

class NoteMemento {
    // TODO: Store content snapshot
    private String name;
    
    public NoteMemento(String name){
        this.name = name;
    }
    public String getName(){
        return name;
    }
}

class NoteHistory {
    // TODO: Use list to store NoteMemento object
    private List<NoteMemento> ans = new ArrayList<>();
    
    public void store(NoteMemento m){
        ans.add(m);
    }
    
    public NoteMemento get(int index){
        return ans.get(index);
    }
    
    // saveVersion(Note note)
    // restoreVersion(int index)
}

public class NoteManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Note obj = new Note();
        NoteHistory obi = new NoteHistory();
        
        int a = sc.nextInt();
        sc.nextLine();
        for(int i=0;i<a;i++){
            String s = sc.nextLine();
            obj.setName(s);
            obi.store(obj.save());
        }
        
         int b = sc.nextInt();
         obj.restore(obi.get(b));
         obj.show();
        sc.close();
    }
}

```






## OUTPUT:
<img width="1042" height="536" alt="image" src="https://github.com/user-attachments/assets/63ba6144-8b00-4cdd-a0ef-b4653335ffb8" />



## RESULT:
The program successfully demonstrates the Memento pattern. Multiple versions of a note are stored, and the content can be restored to any previous version correctly.
