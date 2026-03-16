# Creating Custom Renderables

Build reusable widgets by implementing IRenderable interface.

## Basic Implementation

```csharp
public class MyWidget : IRenderable
{
    public IEnumerable<Segment> Render(IAnsiConsole console)
    {
        yield return new Segment("Hello", Style.Empty);
    }
}
```

## Measure

```csharp
public new Measurements Measure(
    IAnsiConsole console, 
    Constraints constraints)
{
    return new Measurements(10, 1, 10, 1);
}
```

## Full Example

```csharp
public class MyWidget : IRenderable
{
    public string Text { get; }
    
    public MyWidget(string text) => Text = text;
    
    public IEnumerable<Segment> Render(IAnsiConsole console)
    {
        yield return new Segment(Text, Style.Empty);
    }
}
```

## See Also

- Understanding Rendering Model
