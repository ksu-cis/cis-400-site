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

You will need to follow the provided style guide.

Each drink should be declared in the **CowboyCafe** namespace.


### Drink Base Class
Implement an abstract base class to represent any drink.  It should contain properties for: **Price** (a double), **Calories** (an uint), **Ingredients** (a List&lt;string&gt;), **Size**  (using a Size enum, default small), and **Ice** (bool, default true).

### SodaFlavor enum
Implement an enum of flavors for the soda fountain.  Possible flavors are: Cream Soda, Orange Soda, Sarsaparilla, Birch Beer, and Root Beer.

### Jerked Soda Class
Implement a class to represent a Jerked Soda that inherits from the Drink class.  It should have an additional property of **Flavor** with type SodaFlavor.  The price of a Jerked Soda is **$1.59** (small), **$2.10** (medium), and **$2.59** (large).  Calories are **110** (small), **146** (medium), and **198** (large). Special instructions should note "Hold Ice" if served without ice.

## UML Class Diagrams
Create a folder in your solution (not the project) named "Documentation".  Create a single class diagram with all the classes in your Data project.  Save this diagram in the documentation folder and commit it to your repository.
