# TextPath Widget

Display file paths with intelligent truncation and component styling.

## Basic Usage

```csharp
AnsiConsole.Write(new TextPath("/home/user/project/src/main.cs"));
```

## Style

```csharp
new TextPath("/path/to/file")
    .RootStyle(Color.Red)
    .SeparatorStyle(Color.Yellow)
    .StemStyle(Color.Green)
    .ExtensionStyle(Color.Blue);
```

## Alignment

```csharp
new TextPath(path).Alignment(Justify.Right);
```

See: Text Widget
