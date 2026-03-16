# Columns Widget

The Columns widget displays content side-by-side in columns with automatic width distribution.

## Basic Usage

```csharp
AnsiConsole.Write(new Columns(
    "Column 1",
    "Column 2", 
    "Column 3"
));
```

## With Items

```csharp
new Columns(
    new Markup("[yellow]Left[/]"),
    new Markup("[blue]Right[/]")
);
```

## Padding

```csharp
new Columns("Col1", "Col2")
    .Padding(2, 0, 2, 0);
```

## Column Width

```csharp
new Columns("Narrow", "Much wider column here")
    .ColumnWidths(1, 2);  // Ratio
```

## Separator

```csharp
new Columns(items).Separation(2);
```

See: Grid Widget, Rows Widget
