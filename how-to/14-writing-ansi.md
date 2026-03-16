# Writing ANSI

How to write ANSI/VT sequences without the Spectre.Console library.

## Basic ANSI

```csharp
// Colors
Console.Write("\x1b[31m");  // Red
Console.Write("\x1b[0m");     // Reset

// Bold
Console.Write("\x1b[1mBold\x1b[0m");
```

## Color Codes

| Code | Color |
|------|-------|
| 30-37 | Foreground |
| 40-47 | Background |
| 90-97 | Bright FG |
| 100-107 | Bright BG |

## Using AnsiWriter

```csharp
var writer = new AnsiWriter(Console.Out);
writer.Write("Styled", new Style(Color.Red));
```

## Console Extensions

```csharp
Console.Write("\x1b[38;5;196mRed256\x1b[0m");  // 256 colors
Console.Write("\x1b[38;2;255;0;0mTrueColor\x1b[0m"); // RGB
```

## VT Sequences

```csharp
Console.Write("\x1b[2J");     // Clear screen
Console.Write("\x1b[H");       // Home
Console.Write("\x1b[5B");      // Move down 5
```

See: AnsiConsole
