# Align Widget

Control horizontal and vertical alignment of content.

## Basic Usage

```csharp
AnsiConsole.Write(new Align(
    new Text("Center"),
    HorizontalAlignment.Center,
    VerticalAlignment.Middle
));
```

## Horizontal

```csharp
new Align(content, HorizontalAlignment.Left);
new Align(content, HorizontalAlignment.Center);
new Align(content, HorizontalAlignment.Right);
```

## Vertical

```csharp
new Align(content, vertical: VerticalAlignment.Top);
new Align(content, vertical: VerticalAlignment.Middle);
new Align(content, vertical: VerticalAlignment.Bottom);
```

See: Padder Widget
