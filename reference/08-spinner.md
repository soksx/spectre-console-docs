# Spinner Styles Reference

Built-in spinner animations.

## Popular Spinners

| Name | Description |
|------|-------------|
| Dots | Classic dots |
| Line | Simple line |
| Star | Filled star |
| Arc | Arc animation |
| Triangle | Triangle |
| Binary | Binary counter |
| Clock | Clock hands |
| Earth | Rotating earth |

## Usage

```csharp
AnsiConsole.Status()
    .Spinner(Spinner.Known.Dots)
    .Start("Loading...");
```

## Custom

```csharp
new Spinner("_chars", 500);
```
