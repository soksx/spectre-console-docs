# SelectionPrompt

Let users select a single option from a list with keyboard navigation.

## Basic Usage

```csharp
var choice = AnsiConsole.Prompt(
    new SelectionPrompt<string>()
        .Title("Choose a color")
        .AddChoices("Red", "Green", "Blue"));
```

## Page Size

```csharp
.PageSize(10)
```

## More Choices

```csharp
.AddChoices(new[] { "Option1", "Option2", "Option3" })
```

## Without Cancellation

```csharp
.DisableCancelSelection()
```

See: MultiSelectionPrompt, TextPrompt
