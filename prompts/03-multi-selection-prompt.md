# MultiSelectionPrompt

Allow users to select multiple options from a list.

## Basic Usage

```csharp
var toppings = AnsiConsole.Prompt(
    new MultiSelectionPrompt<string>()
        .Title("Choose toppings")
        .AddChoices("Pepperoni", "Mushrooms", "Cheese"));
```

## Not Required

```csharp
.NotRequired()  // Allow no selection
```

## Instructions

```csharp
.InstructionsText("[grey]Use space to toggle[/]");
```

See: SelectionPrompt, TextPrompt
