# Table Widget

The Table widget displays structured data in rows and columns with configurable borders, alignment, and styling.

## When to Use

Use Table when you need to display structured, multi-column data. Common scenarios:

- **Data display**: Show records, configuration settings, or query results
- **Comparison**: Side-by-side feature comparisons or specifications
- **Reports**: Formatted output with headers, totals, and alignment

For simple key-value pairs, consider using a table with hidden headers or a Grid. For proportional data visualization, use BarChart or BreakdownChart.

## Basic Usage

Add columns first, then rows. Each row must have the same number of cells as columns.

```csharp
var table = new Table();

// Add columns
table.AddColumn("Name");
table.AddColumn("Age");
table.AddColumn("City");

// Add rows
table.AddRow("Alice", "28", "New York");
table.AddRow("Bob", "35", "London");
table.AddRow("Charlie", "42", "Tokyo");

AnsiConsole.Write(table);
```

## Styling

### Border Styles

Choose from 18 built-in border styles. Use `RoundedBorder()` for a modern look or `AsciiBorder()` for maximum compatibility.

```csharp
// Different border styles
table.SquareBorder();
table.RoundedBorder();
table.MinimalBorder();
table.HeavyBorder();
table.DoubleBorder();
table.AsciiBorder();
```

### Border Colors

Use BorderColor() to match your application theme:

```csharp
var table = new Table()
    .RoundedBorder()
    .BorderColor(Color.Blue);

table.AddColumn("[yellow]Product[/]");
table.AddColumn("[yellow]Price[/]");

table.AddRow("Widget", "[green]$9.99[/]");
table.AddRow("Gadget", "[green]$19.99[/]");

AnsiConsole.Write(table);
```

## Column Configuration

### Alignment

Align column content with LeftAligned(), Centered(), or RightAligned():

```csharp
table.AddColumn("Left", col => col.LeftAligned());
table.AddColumn("Center", col => col.Centered());
table.AddColumn("Right", col => col.RightAligned());
```

### Width and Padding

Fix column widths with Width(), adjust spacing with PadLeft() and PadRight(), or prevent wrapping with NoWrap():

```csharp
// Fixed width column
table.AddColumn("ID", col => col.Width(5).Centered());

// Column with custom padding
table.AddColumn("Description", col => col.Width(30).PadLeft(2).PadRight(2));

// NoWrap column for long text
table.AddColumn("Status", col => col.NoWrap().RightAligned());
```

## Headers and Footers

Headers display by default. Add footers for totals or summaries:

```csharp
table.AddColumn("Item");
table.AddColumn("Quantity", col => col.RightAligned());
table.AddColumn("Price", col => col.RightAligned());

table.AddRow("Apples", "10", "$5.00");
table.AddRow("Oranges", "5", "$3.50");

// Add footers
table.Columns[0].Footer = new Text("Total", new Style(foreground: Color.Yellow));
table.Columns[1].Footer = new Text("23", new Style(foreground: Color.Yellow));
table.Columns[2].Footer = new Text("$12.50", new Style(foreground: Color.Green, decoration: Decoration.Bold));
```

### Hidden Headers

Tables without headers work well for configuration displays:

```csharp
var table = new Table()
    .HideHeaders()
    .Border(TableBorder.None);

table.AddColumn("Key");
table.AddColumn("Value");

table.AddRow("[blue]Name:[/]", "Application");
table.AddRow("[blue]Version:[/]", "1.0.0");
```

## Titles and Captions

Add context with a title above the table and a caption below:

```csharp
var table = new Table()
    .RoundedBorder()
    .BorderColor(Color.Aqua)
    .Title("[yellow]Monthly Sales Report[/]")
    .Caption("[grey]Data as of October 2025[/]");
```

## Row Formatting

### Row Separators

Use ShowRowSeparators() to add horizontal lines between rows:

```csharp
var table = new Table()
    .RoundedBorder()
    .ShowRowSeparators();
```

### Empty Rows

Insert empty rows to group related data:

```csharp
table.AddRow("[yellow]Header Info[/]", "Data");
table.AddEmptyRow();
table.AddRow("[yellow]Body Info[/]", "Data");
```

## Layout

Use Expand() to fill available console width:

```csharp
var expandedTable = new Table()
    .Expand();
```

## Advanced Usage

### Nested Tables

Embed tables within cells for hierarchical data:

```csharp
// Create inner table
var innerTable = new Table()
    .RoundedBorder()
    .BorderColor(Color.Grey);
innerTable.AddColumn("Detail");
innerTable.AddColumn("Value");
innerTable.AddRow("CPU", "95%");
innerTable.AddRow("Memory", "12GB");

// Create outer table
var outerTable = new Table()
    .SquareBorder();
outerTable.AddColumn("Server");
outerTable.AddColumn("Metrics");

outerTable.AddRow(new Text("server-01"), innerTable);

AnsiConsole.Write(outerTable);
```

### Mixed Content

Cells accept any IRenderable—combine Markup, Panels, and other widgets:

```csharp
var table = new Table().RoundedBorder();

table.AddColumn("Type");
table.AddColumn("Example");

// Markup in cells
table.AddRow(new Text("Markup"), new Markup("[bold green]Success[/]"));

// Panel in a cell
var panel = new Panel("[yellow]Warning[/]")
    .BorderColor(Color.Yellow);
table.AddRow(new Text("Panel"), panel);
```

### Dynamic Updates

Modify tables at runtime with UpdateCell(), InsertRow(), and RemoveRow():

```csharp
// Update cells dynamically
table.UpdateCell(0, 1, new Markup("[green]Complete[/]"));
table.UpdateCell(0, 2, new Markup("[green]100%[/]"));

// Insert a new row
table.InsertRow(3, new Markup("Task 4"), new Markup("[yellow]Pending[/]"), new Markup("0%"));

// Remove a row
table.RemoveRow(2);
```

## See Also

- [Display Tabular Data](/console/how-to/displaying-tabular-data) - Step-by-step guide
- [Table Border Reference](/console/reference/table-border-reference) - All 18 border styles
- [Color Reference](/console/reference/color-reference) - Available colors
