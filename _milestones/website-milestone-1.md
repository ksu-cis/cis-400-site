---
layout: milestone
---
# Website Milestone 1

## Basic Razor Pages
For this milestone you will be creating a website for the CowboyCafe franchise and modifying the Data project to support it.  

Begin by creating a new Razor Pages app named "Website" within your project.  Then implement the requirements listed below.

Beyond these core requirements, you may add features and elements as you see fit.  Moreover, you are encouraged to style the site using CSS.

### General Requirements

You will need to follow the style laid out in the [C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions).

Each new class should be declared in the **CowboyCafe.Website** or **CowboyCafe.Data** namespace, depending on the project it belongs to.

### Privacy Page
Modify the Razor page named _Privacy.cshtml_. It should:

1. Set the page title to "Privacy Policy"
2. Render a `<h1>` tag with the text "Cowboy Cafe Website Privacy Policy"
3. Render the following privacy policy in a `<p>` tag:

_Cowboy Cafe respects and values the privacy of its customers, as we hope you respect and value our own. This site does not collect any data on you. This site does not use cookies. This site only displays information about Cowboy Cafe and its delectable food and delightful trail-rider-themed ambiance._

### About Page
Create a new Razor page named _About.cshtml_.  It should:
1. Set the page title to "About"
2. Render a `<h1>` tag with the text "About Cowboy Cafe"
3. Render the following description in a `<p>` tag:

_Founded in 2020 from the collective collective consciousness of the Spring Semester CIS 400 students of Kansas State University, Cowboy Cafe is devoted to bringing you the finest in trail-rider-themed dining experiences. So pull up a char, partner, and let's wolf down some chow!_

### Layout
Modify the existing *Shared/_Layout.cshtml* to:

1. Set the page title to what is provided by the page with the string "- Cowboy Cafe" concatenated to the end
2. Provide a navigation link to the new About page
3. Change the copyright statement to "(c) 2020 - Cowboy Cafe LLC."

### Error Page
Modify the existing *Error.cshtml* page to:

1. Add the _BuckingBronco.png_ image from the _images.zip_ file available on canvas centered at the top of the page.
2. Underneath that, change the `<h2>` content to "Whoops partner, you just got bucked off by an error!"
3. Remove all text below that point from the page.

**Hint:** to see the error page, you'll need to run the project in release mode.

### Index Page
Modify the existing _Index.cshtml_ page to display the full menu of Cowboy Cafe, following these guidelines:

#### Welcome Message

Add a first-level header (`<h1>`) identifying the page as Cowboy Cafe.

Under that, add a section greeting the customer with the message:

_We at Cowboy Cafe are proud to bring you authentic trail meals from the American West.  Shake off the dust on your boots and sake your thirst with one of our old-fashioned hand-jerked sodas.  Dip your Pan de Campo into a bowl of beans.  Or conquer the the mighty Texas Triple Burger!  You've had a hard ride - so take it easy with us._

#### List the Menu Categories
List the three categories of menu items (Entrees, Sides, and Drinks) using second-level header tags (`<h2>`).

#### List the Menu Items
Below each of the menu category headers, list the items in that category.  Each item should be placed in a `<div>` with a class of `menu-item`.  The `<div>` should include, nested inside, the name of the item, its price, and its calories.  If an item comes in multiple sizes, you will need to list the price and calories for each size.

You may use additional HTML elements to organize and present this information, and use CSS to style it as you see fit.

## Data Project Refactoring
Add a new static class `Menu` to the Data project.  It should implement four static methods:

1. `Entrees()` should return an `IEnumerable<IOrderItem>` containing an single instance (object) of each type of entree served by Cowboy Cafe

2. `Sides()` should return an `IEnumerable<IOrderItem>` containing a single instance (object) of each type of side served at Cowboy Cafe. These can be the default size.

3. `Drinks()` should return an `IEnumerable<IOrderItem>` containing a single instance (object) of each type of drink served at Cowboy Cafe. These can be the default size.

4. `CompleteMenu()` should return an `IEnumerable<IOrderItem>` containing a single instance (object) of each type of item (all entrees, sides, and drinks) served at Cowboy Cafe.  These can be the default size and come with the default Side and Drink.

**HINT:** This `Menu` class can save you a lot of effort in creating the menu item lists for your website.
