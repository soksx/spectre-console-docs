# Understanding Rendering Model

How Spectre.Console renders text and widgets to the terminal.

## Core Concepts

### IRenderable

All visual elements implement IRenderable interface:

```csharp
public interface IRenderable
{
    IEnumerable<Segment> Render(IAnsiConsole console);
}
```

### Measurement

Before rendering, components measure their size:

```csharp
var measured = tree.Measure(console, new Constraints(80, 20));
```

### Rendering Pipeline

1. **Measure** - Calculate size
2. **Render** - Generate segments
3. **Write** - Output to console

## Segmentation

Segments represent styled characters:

```csharp
public class Segment
{
    public string Text { get; }
    public Style Style { get; }
}
```

## Layout

Containers measure children first, then layout:

```csharp
// Table measures each column
// Grid calculates column widths
// Panel wraps content
```

See: API Reference
