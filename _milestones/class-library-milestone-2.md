---
layout: milestone
---

# Class Library Milestone 2

## Add Side Classes and Entree Base Class (100 points possible)

Cowboy Cafe currently offers four sides:

* Chili Cheese Fries (sliced potatoes slathered with chili and cheese)

* Corn Dodgers (a traditional trail treat of fried cornbread)

* Pan de Campo (pan-fried bread)

* Baked Beans (exactly what it sounds like)

For each of these sides, you will need to create a corresponding C# class that inherits from the Side abstract base class (provided).

In addition, you will need to create an abstract base class for Entrees, and refactor your existing entrees to use it.

### General Requirements

You will need to follow the style laid out in the [C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions).

Each side should be declared in the **CowboyCafe.Data** namespace.

Each side should implement a property for: Size (an enum with Small, Medium, and Large options), Price (a double) and Calories (a uint).  The values of these properties varies based on the side's size, as described under each class heading.

Your code should pass all the tests  provided in the DataObjectTest project (note, you will need to uncomment the tests as you write the corresponding classes), and be documented using Visual Studio XML (as specified in the style guide).

### Chili Cheese Fries
Implement a class to represent the Chili Cheese Fries side.  Its price is **$1.99** (small), **$2.99** (medium), and **$3.99** (large).  Its calories are **433** (small), **524** (medium), and **610** (large).

### Corn Dodgers
Implement a class to represent the Corn Dodgers side.  Its price is **$1.59** (small), **$1.79** (medium), and **$1.99** (large). Its calories are **512** (small), **685** (medium), **717** (large).

### Pan de Campo
Implement a class to represent the Pan de Campo side.   Its price is **$1.59** (small), **$1.79** (medium), and **$1.99** (Large). Its calories are **227** (small), **269** (medium), **367** (large).

### Baked Beans
Implement a class representing the Baked Beans side.  Its price is **$1.59** (small), **$1.79** (medium), and **$1.99**. Its calories are **312** (small), **378** (medium), **410** (large).

### Entree Base Class

Create an abstract base class to represent the entrees.  It should define properties for **Price** (double), **Calories** (uint), and **SpecialInstructions** (List<string>) that can be overridden in any derived classes.  Refactor the **CowpokeChili**, **RustlersRibs**, **PecosPulledPork**, **TrailBurger**, **DakotaDouble**, **TexasTriple**, and **Angry Chicken** to derive from this **Entree** base class.
