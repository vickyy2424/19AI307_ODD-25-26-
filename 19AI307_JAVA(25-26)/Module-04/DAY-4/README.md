# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:
To implement Abstract Factory pattern for creating cross-platform UI components (Button, Checkbox) for dark and light themes.

## ALGORITHM :
1.Create abstract factory interface for UI components
2.Implement concrete factories for dark and light themes
3.Create abstract product interfaces for Button and Checkbox
4.Implement concrete products for each theme
5.Let user choose theme and generate corresponding UI components




## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Button {
    void render();
}

interface Checkbox {
    void render();
}

class DarkButton implements Button {
    @Override
    public void render() {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    @Override
    public void render() {
        System.out.println("Dark Checkbox created");
    }
}

class LightButton implements Button {
    @Override
    public void render() {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox {
    @Override
    public void render() {
        System.out.println("Light Checkbox created");
    }
}

interface GUIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

class DarkFactory implements GUIFactory {
    @Override
    public Button createButton() {
        return new DarkButton();
    }
    
    @Override
    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightFactory implements GUIFactory {
    @Override
    public Button createButton() {
        return new LightButton();
    }
    
    @Override
    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();
        
        GUIFactory factory;
        
        if (theme.equals("dark")) {
            factory = new DarkFactory();
        } else if (theme.equals("light")) {
            factory = new LightFactory();
        } else {
            System.out.println("Invalid theme");
            scanner.close();
            return;
        }
        
        Button button = factory.createButton();
        Checkbox checkbox = factory.createCheckbox();
        
        button.render();
        checkbox.render();
        
        scanner.close();
    }
}
```






## OUTPUT:
<img width="572" height="258" alt="image" src="https://github.com/user-attachments/assets/6e6ab92b-f9e4-4489-aca6-7a2bf8736238" />



## RESULT:
The Abstract Factory pattern was successfully implemented. The system correctly generated appropriate Button and Checkbox components based on user's theme selection (dark/light), demonstrating proper creation of themed UI families.




