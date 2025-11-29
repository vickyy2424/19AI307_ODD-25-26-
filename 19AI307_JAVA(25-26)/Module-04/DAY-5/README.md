# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Design a program where a Product model stores item info, and the view displays it. Implement a controller to update product price and refresh the view automatically.



## AIM:
To implement MVC pattern for Product management with automatic view updates when price changes.


## ALGORITHM :
1.Create Product model with item info and price
2.Create View to display product information
3.Implement Controller to handle price updates
4.Use observer pattern for automatic view refresh on model changes
5.Demonstrate price update and view synchronization


## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Vigneshwaran S
RegisterNumber: 212224060301
*/
```

## SOURCE CODE:
```
import java.util.*;

// Model
class Product {
    private String name;
    private double price;
    private String code;
    private List<ProductView> views = new ArrayList<>();
    
    public Product(String name, double price, String code) {
        this.name = name;
        this.price = price;
        this.code = code;
    }
    
    public String getName() {
        return name;
    }
    
    public double getPrice() {
        return price;
    }
    
    public String getCode() {
        return code;
    }
    
    public void setPrice(double price) {
        this.price = price;
        notifyViews();
    }
    
    public void addView(ProductView view) {
        views.add(view);
    }
    
    private void notifyViews() {
        for (ProductView view : views) {
            view.display();
        }
    }
}

// View
class ProductView {
    private Product product;
    
    public ProductView(Product product) {
        this.product = product;
        product.addView(this);
    }
    
    public void display() {
        System.out.println("--- Product Details ---");
        System.out.println("Name : " + product.getName());
        System.out.println("Price: " + product.getPrice());
        System.out.println("Code : " + product.getCode());
    }
}

// Controller
class ProductController {
    private Product product;
    
    public ProductController(Product product) {
        this.product = product;
    }
    
    public void updatePrice(double newPrice) {
        product.setPrice(newPrice);
    }
}

// Main class
public class Main {
    public static void main(String[] args) {
        // Create product model
        Product product = new Product("Laptop", 65000.0, "LP123");
        
        // Create view
        ProductView view = new ProductView(product);
        
        // Create controller
        ProductController controller = new ProductController(product);
        
        // Display initial state
        view.display();
        
        // Update price and see automatic refresh
        controller.updatePrice(62000.0);
    }
}
```






## OUTPUT:
<img width="737" height="305" alt="image" src="https://github.com/user-attachments/assets/854229b5-7573-4631-9a22-4413b525dd9c" />


## RESULT:
The MVC architecture was successfully implemented. The controller updated product prices and the view automatically refreshed to display changes, demonstrating proper separation of concerns and observer pattern functionality.





