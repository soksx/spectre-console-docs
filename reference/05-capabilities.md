# Capabilities Reference

Terminal capabilities and environment detection.

## Auto-Detection

Spectre.Console automatically detects:

- Terminal type
- Color support (16, 256, TrueColor)
- Unicode support
- Interactive mode

## Check Capabilities

```csharp
var console = AnsiConsole.Console;
var capabilities = console.Capabilities;

// Check features
if (capabilities.Unicode)
    // Use Unicode
if (capabilities.ColorSystem == ColorSystem.TrueColor)
    // Full colors
```

## Color System

| System | Colors |
|--------|-------|
| None | No colors |
| Basic | 8 colors |
| Xterm | 256 colors |
| TrueColor | 16M colors |

## Environment

```csharp
System.Environment.GetEnvironmentVariable("TERM");
```
