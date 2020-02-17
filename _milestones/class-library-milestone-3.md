---
layout: milestone
---

# Class Library Milestone 3

## Add Drink Classes and UML (100 points Possible)

Cowboy Cafe currently offers four drinks:

* Jerked Soda (old-fashioned sodas)

* Texas Tea (iced tea)

* Cowboy Coffee (coffee)

* Water (Water)

For each of these drinks, you will need to create a corresponding C# class that inherits from a Drink abstract base class that you will also need to write.

In addition, you will need to draw UML class diagrams for all the classes in your project.

## General Requirements

You will need to follow the style laid out in the [C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions).

Each drink should be declared in the **CowboyCafe.Data** namespace.


### Drink Base Class
Implement an abstract base class to represent any drink.  It should contain properties for: **Price** (a double), **Calories** (an uint), **Ingredients** (a List&lt;string&gt;), **Size**  (using a Size enum, default small), and **Ice** (bool, default true).

### SodaFlavor enum
Implement an enum of flavors for the soda fountain.  Possible flavors are: Cream Soda, Orange Soda, Sarsaparilla, Birch Beer, and Root Beer.

### Jerked Soda Class
Implement a class to represent a Jerked Soda that inherits from the Drink class.  It should have an additional property of **Flavor** with type SodaFlavor.  The price of a Jerked Soda is **$1.59** (small), **$2.10** (medium), and **$2.59** (large).  Calories are **110** (small), **146** (medium), and **198** (large). Special instructions should note "Hold Ice" if served without ice.

### CowboyCoffee Class
Implement a class to represent a Cowboy Coffee that inherits from the Drink class.  It should have an additional properties **RoomForCream** that is false by default, **Decaf** that is false by default, and should have its **Ice** property also false by default.  The price of a CowboyCoffee is **$0.60** (small), **$1.10** (medium), and **$1.60** (large).  Calories are **3** (small), **5** (medium), and **7** (large). Special instructions should note "Add Ice" if served with ice and "Room for Cream" if it should have room for cream.

### TexasTea Class
Implement a class to represent a Texas Tea that inherits from the Drink class.  It should have an additional properties **Sweet** that is true by default and **Lemon** that is false by default.  The price of a TexasTea is **$1.00** (small), **$1.50** (medium), and **$2.00** (large).  Calories are **10** (small), **22** (medium), and **36** (large) for sweet tea, and halved for tea without sweetener. Special instructions should note "Hold Ice" if served without ice and "Add Lemon" if it is served with lemon.

### Water Class
Implement a class to represent a Water that inherits from the Drink class.  It should have an additional property **Lemon** that is false by default.  The price of a water is **0.12** for all sizes, and it has **0** calories for all sizes.  Special instructions should note "Hold Ice" if served without ice and "Add Lemon" if it is served with lemon.

## UML Class Diagrams
Create a folder in your solution (not the project) named "Documentation".  Create a single class diagram with all the classes in your Data project.  Save this diagram in the documentation folder and commit it to your repository.
