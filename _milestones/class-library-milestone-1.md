---
layout: milestone
---

# Class Library Milestone 1

## Add Entree Classes (100 points possible)

Cowboy Cafe currently offers seven entrees:

* Cowpoke Chili (a big bowl spicy chili)

* Rustler's Ribs (BBQ spare ribs)

* Pecos Pulled Pork (BBQ pulled pork sandwich)

* Trail Burger (a 1/4lb burger)

* Dakota Double (a 1/2lb double burger)

* Texas Triple (a 3/4lb triple burger)

* Angry Chicken (spicy BBQ chicken sandwich)

For each of these entrees, you will need to create a corresponding C# class (an implementation for Cowpoke Chili is provided).

### General Requirements

You will need to follow the style laid out in the [C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions).

Each entree should be declared in the **CowboyCafe.Data** namepace.

Each entree should implement a property for: Price (a double), Calories (a uint), and SpecialInstructions (a List<string>).  The list of instructions depends on the class, as described under each class heading.

Your code should pass all the tests  provided in the DataObjectTest project (note, you will need to uncomment the tests as you write the corresponding classes), and be documented using Visual Studio XML (as specified in the style guide).

### Rustler's Ribs
Implement a class to represent the Rustler's Ribs entree.  Its price is **$7.50** and its calories are **894**.  It has no special instructions.

### Angry Chicken
Implement a class to represent teh Angry Chicken entree.  Its price is **$5.99** and its calories are **190**.  It should have boolean properties for **Bread** and **Pickle** which default to true.  When **Bread** is false, the special instructions should include the string **"hold bread"** and when **Pickle** is false, the special instructions should include the string **"hold pickle"**.

### Pecos Pulled Pork
Implement a class to represent the Pecos Pulled Pork entree.  Its price is **$5.88** and its calories are **528**.  It should have boolean properties for **Bread** and **Pickle**, which default to true.  When **Bread** is false, the special instructions include the string **"hold bread"** and when **Pickle** is false, the special instructions should include the string **"hold pickle"**.

### Trailburger
Implement a class representing a Trailburger entree.  It costs **$4.50** and has **288** calories.  It should have boolean properties for **Bun**, **Ketchup**, **Mustard**, **Pickle**, and **Cheese**.  These are true by default.  Setting these to false will create a corresponding instruction in the **SpecialInstructions** list: "hold ketchup", "hold mustard", "hold pickle", and "hold cheese".

### Dakota Double Burger
Implement a class representing a Dakota Double Burger entree.  It costs **$5.20** and has **464** calories. It has all the properties of the Trailburger, plus **Tomato**, **Lettuce**, and **Mayo**.  These too are true by default.  Setting them to false adds the corresponding "hold" instruction to the **SpecialInstructions** property.

### Texas Triple Burger
Implement a class representing a Texas Triple Burger.  It costs **$6.45** and has **698** calories. It has all the properties of the Dakota Double burger, plus **Bacon**,  and **Egg**.  These too are true by default.  Setting them to false adds the corresponding "hold" instruction to the **SpecialInstructions** property.
