# Padder Widget

Add padding around any renderable content.

## Basic Usage

```csharp
AnsiConsole.Write(new Padder(new Text("Text"), Padding.All(2));
```

## Padding Options

```csharp
Padding.All(2)      // 2 on all sides
Padding.Vertical(1)  // 1 top/bottom
Padding.Horizontal(3) // 3 left/right
Padding.Uniform(2)    // Same on all
```

## With Style

```csharp
new Padder(content)
    .Border(PadBorder.None)
    .BorderColor(Color.Blue);
```

See: Align Widget
