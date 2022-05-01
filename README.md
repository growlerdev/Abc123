# Abc123

[![NuGet version (iAutomateDesign.AutodeskAppStore)](https://buildstats.info/nuget/Abc123)](https://www.nuget.org/packages/Abc123)

Infinitely correlates an array of characters to a zero based index. When the index exceeds the length of the character array, a prefix is recursively added.

## Usage

The default character array is the English Alphabet.

```csharp
var alphaSvc = new AlphaNumericService();

alphaSvc.GetString(0); //--> returns "A"
alphaSvc.GetString(1); //--> returns "B"
alphaSvc.GetString(2); //--> returns "C"

alphaSvc.GetString(26); //--> returns "AA"
alphaSvc.GetString(777); //--> returns "ACX"
```

### Overriding Default Character Array

The character array can be overridden by passing in a string into the `AlphaNumericService` constructor.

```csharp
var alphaSvc = new AlphaNumericService("SOMETEXT");

alphaSvc.GetString(0); //--> returns "S"
alphaSvc.GetString(1); //--> returns "O"
alphaSvc.GetString(2); //--> returns "M"

alphaSvc.GetString(8); //--> returns "SS"
```

## Release Notes

### 1.1.2

* Included Source Repository in NuGet Package
* Added License file

### 1.1.1

* Updated README

### 1.1.0

* Initial Release