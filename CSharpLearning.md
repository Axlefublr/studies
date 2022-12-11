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

You can cast values to different values with

```cs
byte byt = (byte) int.Parse(Console.Readline());
```

That even works for stuff like `enum`s and likely classes and stuff

You can use `checked ()` to make sure the type casting doesn't cut the information stored in the variable. 
Will throw an error we can catch if it does.

Instead of `Convert`, you can use `type.Parse` to parse into that type. 
`.TryParse` returns a boolean on whether or not the information was cut

Use `var` for when you don't know the type the variable is going to be / it doesn't matter

It requires you to initialize the variable straight away though

## Type getting

By using the `GetType()` method, you can see what type something is, but it's not as legible as `int` or `string`, it's `System.Int32` and the like

By using `typeof()` you can get the "System.Whatever" version of the type, that can be compared nicely with the GetType() thing

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

## Types of numbers and their possible values

![](img/different%20types%20of%20numbers.png)

![](img/different-types-of-numbers-2.png)

Types have two useful properties: `MinValue` and `MaxValue`

So, you can just have the code tell you what you should use, rather than looking it up

## Enums

By default, uses `int`

By default, start a `0` and increment by one

Even if you make the second key equal to 1, for example, that won't change the first one being zero by default

`Weekdays.Monday` would just give its name (as a string)

`(int)Weekdays.Monday` would give us the integer of monday (zero by default)

You can make keys be equal to other keys.
No need to specify the `enum` "class" in that case either

## Byref

`in` keyword

Protects data from being changed, making it readonly

Some things are passed by reference by default (so you don't really need to return them even)

Stuff like `enum`s and arrays

So you could use `void` and return nothing, that will still change what you passed, no need to 

`int[] array = Method(array);`

If you want to introduce this behavior to stuff that gets passed by value, use `ref`

`out` is essentially return. I don't like it but it does exist. Yeah, it is also by reference

## By values vs by reference types

![](img/by-value-vs-by-reference.png)

## Properties

```cs
class Human {
   private int age;
   public int Age {
      get {
         return age;
      }
      set {
         age = value;
      }
   }
}
```

The reason for this existing: you can have logic surrounding both actions, that could either do something else required as well, or check the type, or whatever else

If you just just made `age` public and interacted with it directly, you wouldn't be able to program in specific behavior

That said, that can often be unnecessary

## Access modifiers

`sealed` removes the ability to extend (make a child of) the class

makes the current overriden method the final override, not letting you override it again in a child class

`internal` - access to the class only in the same project

`private` - access only within the class

`public` - accessible from anywhere

`protected` - accessible from within the class and all its children

`private protected` - either private, or accessible by a child class, but only in the same project

## Polymorphism

`virtual` - this method can be overriden in a child class

`override` - this method overrides this same method in a parent class

`new` - method hiding

## Overriding operators 

These operators are available for overriding

![](img/Overriding-parameters.png)

These `+=, -=, *=, /=, %=, &=, |=, ^=, <<=, >>=` operators can't be overriden, but use the overrides of the operators they use

## MethodBase.GetCurrentMethod()

Returns a `System.Reflection.MethodBase` object that has information about the current method

## System.IO

### .DriveInfo

`GetDrives()` returns an array

`AvailableFreeSpace` указывает на объем доступного свободного места на диске в байтах;

`DriveFormat`        получает имя файловой системы;

`DriveType`          представляет тип диска;

`IsReady`            готов ли диск (например, DVD-диск может быть не вставлен в дисковод);

`Name`               получает имя диска;

`TotalFreeSpace`     получает общий объем свободного места на диске в байтах;

`TotalSize`          общий размер диска в байтах;

`VolumeLabel`        получает или устанавливает метку тома.

### .Directory

`CreateDirectory(path)`     создает каталог по указанному пути;

`Delete(path)`              удаляет каталог по указанному пути;

`Exists(path)`              определяет, существует ли каталог по указанному пути;

`GetDirectories(path)`      получает список каталогов в каталоге path;

`GetFiles(path)`            получает список файлов в каталоге path;

`Move(source, destination)` перемещает каталог;

`GetParent(path)`           получение родительского каталога.

### .DirectoryInfo

`Create()`                 создает каталог;

`CreateSubdirectory(path)` создает подкаталог по указанному пути path;

`Delete()`                 удаляет каталог;

Свойство `Exists`          определяет, существует ли каталог;

`GetDirectories()`         получает список каталогов;

`GetFiles()`               получает список файлов;

`MoveTo(destDirName)`      перемещает каталог;

Свойство `Parent`          получение родительского каталога;

Свойство `Root`            получение корневого каталога.

### .File

static, so used for one-off operations

### .FileInfo

requires an object, so used for multiple operations

## Serialization

`[Serializable]` before the class to make it serializable

`[NonSerialized]` mark specific parts of the class as not serializable