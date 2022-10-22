## Char type

`char` is for a single character (string)

## String vs char quotes

Char uses `''`

String uses `""`

## Type conversion

`Convert` class

A variable's type can only be one thing, so you *have to* use a different variable when converting

```cs
string nummy = "5";
int num = Convert.ToInt32(nummy);
```

## Type getting

By using the `GetType()` method, you can see what type something is, but it's not as legible as `int` or `string`, it's `System.Int32` and the like

## Random requires an object

```cs
Random random = new Random();
random.Next(); //generate an int
random.NextDouble();
```

With no parameters, generates from 1 to max int

## fstrings in C#

`$"This is text, this is a {variable}"`

## Creating a project

`dotnet new sln -n "name"` create a solution (won't create another folder)

`dotnet new console -n "name"` create a project folder (will create another folder named as the name)

`dotnet new classlib -n "name"` class library

`dotnet sln solutionFile.sln add **/*.csproj` add all the projects below the current folder into the solution

`dotnet add Main/Main.csproj reference Library/Library.csproj` add a reference to the library project to the main project

`dotnet add package PackageName` to add a nuget package

## Escaping special symbols

`\x23` for ascii

`\u1234` for unicode

## Different numbers

![](img/different%20types%20of%20numbers.png)

![](img/different-types-of-numbers-2.png)

Types have two useful properties: `MinValue` and `MaxValue`

So, you can just have the code tell you what you should use, rather than looking it up
