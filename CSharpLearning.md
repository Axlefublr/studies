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