# JsonText Widget

The JsonText widget renders JSON data with syntax highlighting.

## Basic Usage

```csharp
var json = @"{
    ""name"": ""John"",
    ""age"": 30
}";
AnsiConsole.Write(new JsonText(json));
```

## Syntax Highlighting

JSON is automatically highlighted:
- Keys: Yellow
- Strings: Green
- Numbers: Blue
- Booleans: Red

## Collapsed

```csharp
new JsonText(json).Collapsed();
```

## With Options

```csharp
new JsonText(json)
    .HighlightKeys()
    .Valid();
```

See: Canvas Widget
