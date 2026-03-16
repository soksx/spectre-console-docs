# Box Border Reference

Complete reference of all box border styles.

## Available Borders

| Style | Description |
|-------|-------------|
| None | No border |
| Square | Standard square corners |
| Rounded | Rounded corners |
| Heavy | Heavy lines |
| Double | Double lines |
| Ascii | ASCII characters |
| Minimal | Minimal borders |

## Usage

```csharp
new Panel("Content").Border(BoxBorder.Rounded);
new Table().Border(TableBorder.None);
```

## Custom

```csharp
new BoxBorder('*', '*', '-', '|');
```
