# Displaying Tabular Data

Display structured data in tables with borders, alignment, and styling.

## Basic Table

```csharp
var table = new Table();
table.AddColumn("Name");
table.AddColumn("Age");
table.AddRow("Alice", "30");
table.AddRow("Bob", "25");
AnsiConsole.Write(table);
```

## Border Styles

```csharp
table.RoundedBorder();
table.MinimalBorder();
table.HeavyBorder();
```

## Alignment

```csharp
table.AddColumn("Name", c => c.RightAligned());
```

## Title & Caption

```csharp
table.Title("Users");
table.Caption("Total: 2 users");
```

See: Table Widget
