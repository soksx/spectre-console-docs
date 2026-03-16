# Grid Widget

The Grid widget arranges content in rows and columns without visible borders.

## Basic Usage

```csharp
var grid = new Grid();
grid.AddColumn();
grid.AddColumn();
grid.AddRow("Name:", "John");
grid.AddRow("Email:", "john@example.com");
AnsiConsole.Write(grid);
```

## Column Widths

```csharp
grid.AddColumn(new GridColumn { Width = 15 });
grid.AddColumn(new GridColumn { Width = 40 });
```

## Alignment

```csharp
new GridColumn { Alignment = Justify.Right };
```

## Expand

```csharp
new Grid { Expand = true }
```

## See Also

- Table Widget - With visible borders
- Columns Widget - Auto-flowing columns
