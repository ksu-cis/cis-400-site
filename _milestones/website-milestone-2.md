---
layout: milestone
---
# Website Milestone 2

## Searching and Filtering
For this milestone you will modifying your Index page to allow users to search and filter the displayed menu.

Beyond these core requirements, you may add features and elements as you see fit.  Moreover, you are encouraged to style the site using CSS.

### General Requirements

You will need to follow the style laid out in the [C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions).

Each new class should be declared in the **CowboyCafe.Website** or **CowboyCafe.Data** namespace, depending on the project it belongs to.

### Search and Filter Form

Add a form to your _Index.cshtml_ page. that contains inputs for:
1. A submit button to run the search and filter operations
2. A text input to enter search terms into
3. A series of checkboxes corresponding to the types of order items (Entree, Side, and Drink)
4. Two number inputs specifying a range that calories should fall into
5. Two number inputs specifying a range that price should fall into.

Each of these additional inputs should be arranged so that their purpose and use is clear to the casual web surfer.  I.e. they should be clearly labeled and ordered.  Look at your Movie site for ideas.

In addition, any search terms or filter values that are set should persist (reappear) when a search operation is run.

Finally, the results listed on the page should be only those that fit the search and filtering criteria (unless none have been set, in which case the full menu should be displayed).

### Search and Filter functionality

The Searching and Filtering functionality should be implemented in your `Menu` class in the Data project as static methods.  Each of these methods should take an `IEnumerable<IOrderItem>` as its starting collection, and return an `IEnumerable<IOrderItem>` that is the filtered or searched collection.  If the filter options or search term is null, then the original collection should be returned.

The suggested structure for the Menu class is represented in the UML class diagram, below:

![The Menu Class UML]("assets/web-ms-2.1.png")


### Testing the Menu Properties

You should add tests to verify that the menu Properties (`Entrees`, `Sides`, and `Drinks`) operate as expected, and return a collection containing one instance of each menu item in that category.  

Also, test that the `All` property returns a collection containing one instance of every item on the menu.

These do not need to include permutations (i.e. different sizes, different flavors) unless you choose to do so.  If that is your implementation, you should test for all the corresponding permutations.

### Testing the Menu Search and Filter Methods

You should add tests to verify that the search and filtering functions operate as expected.  Remember to test both valid and null values for all parameters.
