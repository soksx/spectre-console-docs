# Text Widget

The Text widget renders text content with programmatic control over styling, justification, and overflow behavior.

## Basic Usage

```csharp
var plain = new Text("Hello, World!");
AnsiConsole.Write(plain);

var styled = new Text("Styled", new Style(foreground: Color.Blue));
AnsiConsole.Write(styled);
```

## Justification

```csharp
new Text("Text").LeftJustified()
new Text("Text").Centered()  
new Text("Text").RightJustified()
```

## Overflow

```csharp
new Text(longText).Overflow(Overflow.Fold)     // Wrap
new Text(longText).Overflow(Overflow.Crop)     // Truncate
new Text(longText).Overflow(Overflow.Ellipsis) // Truncate with ...
```

## Styling

```csharp
new Style(foreground: Color.Blue)           // Foreground
new Style(background: Color.Yellow)         // Background
new Style(decoration: Decoration.Bold)     // Decoration
```

See: Markup Widget, Color Reference
