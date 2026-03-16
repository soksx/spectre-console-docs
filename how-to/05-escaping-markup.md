# Escape Markup

Safely display user input, array indexers, and JSON without markup parsing errors.

## Problem

```csharp
var userInput = "Text with [brackets]";
AnsiConsole.MarkupLine(userInput); // ERROR!
```

## Solution

```csharp
var safe = Markup.Escape(userInput);
AnsiConsole.MarkupLine(safe);
```

## Remove Markup

```csharp
var plain = Markup.Remove(styledText);
```

## When to Use

- User input
- JSON data
- Code snippets with brackets

See: Markup Widget
