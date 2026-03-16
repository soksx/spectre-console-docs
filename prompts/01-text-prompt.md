# TextPrompt

Prompt users for text input with validation and default values.

## Basic Usage

```csharp
var name = AnsiConsole.Ask<string>("What's your name?");
```

## With Default

```csharp
var color = AnsiConsole.Ask<string>("Favorite color?", "Blue");
```

## With Validation

```csharp
var email = AnsiConsole.Ask<string>(
    "Enter email:", 
    x => x.Contains("@") ? null : "Invalid email");
```

## Secret Input

```csharp
var password = AnsiConsole.Ask<string>("Password?");
```

See: SelectionPrompt, Confirm
