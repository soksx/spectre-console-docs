# Text Style Reference

Comprehensive reference of text styles and decorations.

## Decorations

| Name | Description |
|------|-------------|
| Bold | Bold text |
| Dim | Dimmed text |
| Italic | Italic text |
| Underline | Underlined |
| Strikethrough | Strikethrough |
| Blink | Blinking text |
| Reverse | Reverse colors |
| Hidden | Hidden text |

## Usage

```csharp
new Style(decoration: Decoration.Bold);
new Style(decoration: Decoration.Italic);
new Style(decoration: Decoration.Bold | Decoration.Italic);
```

## Combined

```csharp
new Style(
    foreground: Color.Red,
    decoration: Decoration.Bold | Decoration.Underline
);
```
