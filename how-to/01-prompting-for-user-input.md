# Prompting for User Input

Collect input from users with text prompts, confirmations, and selection menus.

## Text Prompt

```csharp
var name = AnsiConsole.Ask<string>("What's your name?");
```

## With Default

```csharp
var color = AnsiConsole.Ask<string>("Favorite color?", "Blue");
```

## Confirmation

```csharp
if (AnsiConsole.Confirm("Continue?"))
{
    // Do something
}
```

## Selection

```csharp
var choice = AnsiConsole.Prompt(
    new SelectionPrompt<string>()
        .AddChoices("One", "Two", "Three"));
```

See: SelectionPrompt, MultiSelectionPrompt, TextPrompt
