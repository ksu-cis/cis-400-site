---
layout: default
title: "Style Guide"
---

# CIS 400 Style Guide (Extension of CIS 300)

Authors: Dr. Rodney Howell and Zachery Brunner

## General Definitions:

### Camel Case:

Multiple words are joined without spaces, using capital letters at the beginning of each word excluding the first letter of the first word.

For Example: averageAge, contextBoundObject, rgbCode

## File Consistency:

The easiest way to format a file consistently (after removing all syntax errors) is to select from the “Edit” menu, “Advanced -> Format Document,” then you are able to make changes as necessary.

# Brace Formatting:

* All braces should occur on lines by themselves

  * The exception to this rule is when only one statement is enclosed in the braces

* The “to-do” are executable statements that should be indented 1 further than the encapsulating lines.

## Examples:

```csharp
/*
    The executable statements take up more than one line of code and therefore need to be indented once and on seperate lines
*/

///<Summary>
///This method is an example of the correct way to write a          multiline conditional statement
///</Summary>

private int GlobalExampleInteger;
public void SystemCheck()
{
    if(true)
    {
        GlobalExampleInteger = 0;
        Console.WriteLine("This is how to correctly write a multi-line conditional statement.");
    }
}
```

```csharp
/*
    The executable statements take up only one line of code and therefore should be written one of two different ways.
*/

///<Summary>
///The below method demostrates the first correct way to write a one-line conditional "to-do"
///</Summary>
public int FirstWayToDoOneLineConditionals()
{
    int randomInt = 0;

    //Getters and Setters should be written as follows
    if(true) { return randomInt; }
}


///<Summary>
///The below method demostrates the second correct way to write a one-line conditional "to-do"
///<Summary>
public void SecondWayToDoOneLineConditionals()
{
    if(true)
        Console.WriteLine("Notice how there are no surronding braces and how the line is still indented");
}
```

## Notes:

I will not count off for including the first brace on the same line however, the last brace must be vertically alligned with the beginning of the conditional statement.

```csharp
///<Summary>
///This method demonstrates how to do the same-line brace method
///</Summary>
public void SameLineBrace() {
    Console.WriteLine("This is the CIS 400 Style Guide");
}
```

# Access Modifiers:

C# provides 4 access modifiers for classes, fields, ect. If a modifier is not assigned the default one will be assigned by the compiler. To avoid confusion you will be required to assign them as they are declared except where C# does not allow them. (Namespaces, Members of Interfaces, Local Variables within Methods).

## public:

* Made available throughout the entire program

* All classes should be declared public unless otherwise told

* Some methods but not all methods should be declared public

* NO variables should be declared public, you should use getters and setters to access global variables outside the current class

## private:

* Conceals information from the rest of the program excluding the class that it is declared in

* All global variables should be declared private

* All methods that are internal to the class should be declared private

  * Internal means not called outside of the class it is created in

## internal:

* You should not use this modifier unless explicitly told to do so

## protected:

* You should not use this modifier unless explicitly told to do so

# Naming Conventions:

Always use names that are informational. There should be absolutly no ambiguity when naming variables, classes, and interfaces. While this does make your code “longer” it improves maintainability and readability.

## Examples:

```csharp
///Namespaces: should be informative and not misleading. Pascal case should be used.

using System;
namespace Ksu.Cis400.ThisIsANamespaceExample;
{
    class ExampleClass
    {
        public static void Main(string[] args)
        {
            Console.WriteLine("This is a namespace example");
        }
    }
}
```

```csharp
///Interfaces: The name should always preceed with the letter "I" and then pascal case afterwards

public interface IAmAnInterfaceExample
{

}
```

```csharp
///Classes, Structures, and Enumerations: Use pascal case. If the name begins with the letter "I" the following letter must not be capitalized as this would look like an interface.

public class AccountController
{

}

public class IamNotAnInterface
{

}
```

```csharp
///Methods: The name should be descriptive towards the method it is describing and pascal case should be used.

public void ThisMethodExampleDoesNothing()
{

}
```

# Variable and Control Form Naming Conventions:

## Controls on forms:

Use camel case and begin names with “ux” followed by a capital letter. Make your names descriptive of the functionality, not the type of control. For example, uxAccept, uxCustomerName. (You will not typically declare these names in code, but will enter them in the Visual Studio® design window).

## Public Constants:

Should be descriptive, capitalized all the way through with underscores seperating the words.

```csharp
///<Summary>
///This is the example for a constant field names
///</Summary>
public const int THIS_IS_A_CONST_INT = 100;
```

## Private Fields:

Should be descriptive and use pascal case

```csharp
///<Summary>
///This is the example for private field names
///</Summary>
private double WeightOfAthlete;
```

## Parameters and Local Variables within methods:

Should be descriptive and use camel case

```csharp
///<Summary>
///This is the example for parameters and local variables
///</Summary>
///<Param name="inString">An example string parameter</Param>
///<Param name="inInt">An example integer parameter</Param>
///<Returns>An example string</Returns>
public string ExampleMethod(string inString, int inInt)
{
    string outString = "Camel case should be used for local variables and parameters";
    return outString;
}
```

# Comments:

At the top of each file, add a comment of the following form:

```csharp
/*  The name of the file
*   Author: Your First and Last Name
*/
```

If you are not the original author add the following line

```csharp
*   Modified by: Your First and Last Name
```

Prior to each class, structure, enumeration, field, property, and method type “///” and the IDE will automatically insert the following into the code snippits.

```csharp
///<Summary>
///
///</Summary>
```

Inbetween the <Summary> tags is where you will write the summary of the program component you are documenting. A full stack comment looks as follows.

```csharp
/// <Summary>
/// Computes the number of times a given string x
/// occurs within a given string y.
/// </Summary>
/// <Param name="x">The string being searched for.</Param>
/// <Param name="y">The string being searched.</Param>
/// <Returns>The number of occurrences of x in y.</Returns>
private int Occurrences(string x, string y)
{
	"to-do";
}
```

# Prohibited Features:

The following features of C# should not be used on assignments or exams:

* The goto statement: It has been 50 years since Dijkstra published “Go To Statement Considered Harmful” (Communications of the ACM, vol. 11 (1968), pp. 147-148).

* The unsafe keyword: The name pretty much says it all

* The var keyword: There are very few contexts in which this is needed, and these contexts won’t occur in this class. For all other contexts, it makes the code less readable.

* Virtual methods: These are useful in large-scale software development. However, they are overused. They will not be needed in the programming we will be doing. (However, virtual methods in the .NET class library may be overridden

*    Extension methods: These methods are not defined within the class on which they operate.
