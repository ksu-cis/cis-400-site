---
layout: milestone
---

# Point of Sale Milestone 3

## Customizing Orders

For this milestone, you will be expanding the Cowboy Cafe Point of Sale project and the Data project.  These expansions will allow a user to customize individual order items using the user interface.

### General Requirements

You will need to follow the style laid out in the [C# Coding Conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions).

Each new class should be declared in the **CowboyCafe.PointOfSale** or **CowboyCafe.Data** namespace, depending on the project it belongs to.

### Part 1: Add Order Item Customization Controls

At this point, you will be creating customization controls for each of the types of order items.  These should inherit from `UserControl`, and display the customizable attributes of the order item in appropriate controls (i.e. buttons, selection drop-downs, radio buttons, checkboxes) of your choosing.

These will need to edit a specific instance of an `IOrderItem` corresponding to the control, i.e. if we are working with the `CowpokeChili`, you should have a control that allows us to set the `Cheese`, `SourCream`, and `GreenOnion` properties to `true` or `false`.  You will need to make the instance available to the control (this can be done through data binding, a constructor argument, or by a method or property).

You may optionally combine related `IOrderItems` into a single customization `UserControl`, but if you do so, you need to only display the controls related to that specific order item (i.e. if you made a Drink customization control, it should not display flavor selection when customizing a Texas Tea).

### Part 2: Add Screen Switching

When the user clicks a specific "Add Item" button in your `SelectMenuItem` control, you should load the corresponding customization control to customize the item (The item you are editing should be the same instance that was added to the order).

When the user clicks the "Select Menu Items" button in your `OrderControl`, you should return to/load a new `MenuItemSelectionControl`, allowing more additions to the order.

An easy way to establish this screen switching is to create a `Border` object in your `OrderControl` with an assigned name property.  Then you can swap out what this `Border` contains by setting `Border.Child` to the specific control you want to display.

Note that your various customization controls will need to be able to send messages to the `OrderControl` to let it know that it needs to load a different screen.  The `Parent` property will come in handy here.

### Part 3: INotifyPropertyChanged Implementation

For the changes to your `IOrderItem`s to appear in the `OrderSummaryControl`, you will need to implement the `INotifyPropertyChanged` interface on all order items.  For example, when the `CowpokeChili.Cheese` property is set to false, it will need to notify that the `"Cheese"` property has changed.

Moreover, your `Order` class will need to subscribe to these notifications on each item added to itself (and unsubscribe when the item is removed), and upon receiving a property change notification, notify that its own `Items` property (and possibly `Price` property) have changed.  This event bubbling is necessary for the `OrderSummary` to display the updated order characteristics.

### Part 4: Update UML
Finally, you should update your UML diagrams to reflect the new classes in the _PointOfSale_ and _Data_ projects.
