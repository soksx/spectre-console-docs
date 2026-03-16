# Rows Widget

The Rows widget stacks multiple renderables vertically with consistent spacing.

## Basic Usage

```csharp
AnsiConsole.Write(new Rows(
    "First item",
    "Second item",
    "Third item"
));
```

## With Styling

```csharp
new Rows(
    new Markup("[yellow]Header[/]"),
    new Markup("Content here")
).Separation(2);
```

See: Columns Widget
