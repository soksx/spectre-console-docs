# FigletText Widget

The FigletText widget creates large ASCII art text banners.

## Basic Usage

```csharp
var figlet = new FigletText("Hello")
    .LeftJustified();
AnsiConsole.Write(figlet);
```

## Fonts

```csharp
new FigletText("Text", FigletFonts.Small);
new FigletText("Text", FigletFonts.Standard);
new FigletText("Text", FigletFonts.Big);
```

## Color

```csharp
new FigletText("Text")
    .Color(Color.Aqua);
```

See: Text, Markup
