# CasualDev.Numerics
Adds a "real" type (real number) to represent a floating point number with unlimited decimal precision.
\n


## Overview

CasualDev.Numerics is a library for C# developed on the **.NET 8.0** framework.
It utilizes a custom type of "real" (derived from "real number") which is a floating point number with unlimited decimal precision.
This type can be used for complex mathematical equations that require extreme precision. 

Along with this type the library includes a Mathf class with a built in PI "real", this "Mathf.PI" is PI to 9877 decimal places, which is approximately 32,768 bits of data.
In the future, more Mathf functions to allow "real" values to be used in sin, cos, tan, cot, log, abs, mod (etc.) equations.


## Installation

#### Installation for Visual Studio Community or .NET CLI:
Ensure that your project is set up as a **Console Application**, and paste the following code into the Terminal (Package Manager Console on VS).
###### If at any point you get an error, make sure to check that the directory you are running your command in is the root directory of your project.
```powershell
dotnet add package CasualDev.Numerics --version 1.0.1
```

Then, inside of your .cs file, paste the following at the top:
```cs
using CasualDev.Numerics;
```

For different IDEs or methods of installing this library, you can visit the [NuGet Repository](https://www.nuget.org/packages/CasualDev.Numerics) and view more installation methods from there.


## Syntax

"real" values are written as strings, and then is converted into a floating point number when preforming arithmetic calculations.
The correct syntax when declaring a variable of type "real" is:
```cs
// real {variableName} = "{valueAsString}";
```

Performing calculations on two "real" numbers together is the same as performing calculations two regular integers or floating point numbers.
```cs
real num1 = "2.1858589201998582819549952";
real num2 = "9.2857572717898958209889018985887683992";

Console.WriteLine(num1 + num2);
// Output: 11.4716161919897541029438970985887683992
Console.WriteLine(num1 * num2);
// Output: 20.29735536335264364117034643091156638827948900859439437034768384
```

Variables of type "real" can be concatenated and interpolated with normal strings.

## Mathf
Mathf is a custom Math class that is integrated to work with "real" variables.
In later versions of this library, more methods that allow features like Mathf.Sin(), Mathf.Cos(), Mathf.Tan(), Mathf.Cot(), Mathf.Abs(), Mathf.Mod() and Mathf.Pow() will be added.

Mathf.PI is a constant real type variable, this variable contains the digits of pi to 9877 decimal places. This can be used for extremely complicated equations that require insane amounts of precision.
