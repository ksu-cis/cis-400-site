---
layout: milestone
---

# Menu Milestone 2

## Add Side Classes + Abstract Base Classes (100 points Possible)

DinoDiner currently offers four sides:

* Fryceritops (French Fries)

* MeteorMacAndCheese (Macaroni and Cheese with Sausages)

* Mezzorella Sticks (Fried Breaded Motzorella Sticks)

* Triceritots (Tater Tots)

For each of these sides, you will need to create a corresponding C# class that inherits from the Side abstract base class (provided).

In addition, you will need to create an abstract base class for Entrees, and refactor your existing entrees to use it.

## General Requirements

You will need to follow the provided style guide.

Each side should be declared in the **DinoDiner.Menu.Side** namespace.

Each Side should implement a property for: **Price** (a double), **Calories** (an uint), **Ingredients** (a List&lt;string&gt;), and **Size**  (using the Size enum).

Your code should pass all the tests provided in the MenuTest project, and be documented using Visual Studio XML (as specified in the style guide).

### Fryceritops (15 points)

Implement a class to represent the Fryceritops Side that inherits from the Side base class.  It’s price is **$0.99 (small)**, **$1.45 (medium)**, or **$1.95 (large)**.  Its calories are **222 (small)**, **365 (medium)**, and **480 (large)**.  Its ingredients are **potatoes, salt,** and **vegtable oil**.

### MeteorMacAndCheese (15 points)

Implement a class to represent the MeteorMacAndCheese Side that inherits from the Side base class.  It’s price is **$0.99 (small)**, **$1.45 (medium)**, or **$1.95 (large)**.  Its calories are **420 (small)**, **490 (medium)**, and **520 (large)**.  Its ingredients are **macaroni noodles, cheese product,** and **pork sausage**. 

### MezzorellaSicks (15 points)

Implement a class to represent the MezzorellaSticks Side that inherits from the Side base class.  It’s price is **$0.99 (small)**, **$1.45 (medium)**, or **$1.95 (large)**.  Its calories are **540 (small)**, **610 (medium)**, and **720 (large)**.  Its ingredients are **cheese product, breading,** and **vegtable oil**. 

### Triceritots (15 points)

Implement a class to represent the Triceritots Side that inherits from the Side base class.  It’s price is **$0.99 (small)**, **$1.45 (medium)**, or **$1.95 (large)**.  Its calories are **352 (small)**, **410 (medium)**, and **590 (large)**.  Its ingredients are **potatoes, salt,** and **vegtable oil**. 

### Entree Base Class (10 points)

Create an Entree base class in the DiniDiner.Menu.Entrees namespace.  It should be an abstract class, and include Properties for **Price, Calories,** and read-only **Ingredients**.

### Refactoring Entree Classes (20 points)

Refactor your existing Entree classes to inherit from the Entree base class.
