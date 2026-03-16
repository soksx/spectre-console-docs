# Panel Widget

The Panel widget creates bordered boxes around content with customizable headers, padding, and styles.

## Basic Usage

```csharp
var panel = new Panel("Hello, World!")
    .Header("Greeting")
    .Border(BoxBorder.Rounded);

AnsiConsole.Write(panel);
```

## Border Styles

```csharp
new Panel(content).SquareBorder();
new Panel(content).RoundedBorder();
new Panel(content).MinimalBorder();
new Panel(content).HeavyBorder();
new Panel(content).DoubleBorder();
new Panel(content).Border(TableBorder.None);
```

## Header & Footer

```csharp
new Panel(content)
    .Header("[yellow]Title[/]")
    .Footer("Footer text");
```

## Padding

```csharp
new Panel(content).Padding(1, 2, 1, 2);  // left, top, right, bottom
```

## Expand

```csharp
new Panel(content).Expand();  // Fill available width
```

See: Grid Widget, Table Widget
