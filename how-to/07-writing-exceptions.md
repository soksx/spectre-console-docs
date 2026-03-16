# Write Exceptions

Display formatted exception details with stack traces, colors, and clickable links.

## Basic Usage

```csharp
try {
    // code that throws
} catch (Exception ex) {
    AnsiConsole.WriteException(ex);
}
```

## Custom Style

```csharp
AnsiConsole.WriteException(ex, new ExceptionSettings
{
    Format = ExceptionFormats.ShortTypeWhichMessage,
    Style = new ExceptionStyle
    {
        Exception = new Style(Color.Red),
        Message = new Style(Color.White)
    }
});
```

## Format Options

```csharp
ExceptionFormats.Default              // Full exception
ExceptionFormats.SimpleMessage       // Just message
ExceptionFormats.ShortTypeWhichMessage // Type: Message
```

See: Markup Widget
