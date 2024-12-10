# Abc123

![GitHub Release](https://img.shields.io/github/v/release/growlerdev/abc123?display_name=release&logo=github&label=release&link=https%3A%2F%2Fgithub.com%2Fgrowlerdev%2Fabc123%2Freleases)
    ![GitHub Release](https://img.shields.io/github/v/release/growlerdev/abc123?include_prereleases&display_name=release&logo=github&label=latest%20build&link=https%3A%2F%2Fgithub.com%2Fgrowlerdev%2Fabc123%2Freleases)
    ![NuGet Downloads](https://img.shields.io/nuget/dt/abc123?logo=nuget&color=9932CC)
    ![GitHub License](https://img.shields.io/github/license/growlerdev/abc123?color=salmon)
    ![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/growlerdev/abc123/main.yml?logo=githubactions&logoColor=white&label=Build%20and%20Deploy&link=https%3A%2F%2Fgithub.com%2Fgrowlerdev%2Fabc123%2Factions%2Fworkflows%2Fbuild-deploy.yml)

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

## Change Log

### 1.3.1

* Updated to target .NET Standard 2.0
