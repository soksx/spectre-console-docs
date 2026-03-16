# Justify Widget

The Justify widget aligns content within a fixed width.

## Basic Usage

```csharp
AnsiConsole.Write(new Justify("Text", 20, Justify.Center));
```

## Alignment

```csharp
new Justify("Text", 20, Justify.Left);
new Justify("Text", 20, Justify.Center);
new Justify("Text", 20, Justify.Right);
```

## With Markup

```csharp
new Justify(new Markup("[green]Success[/]"), 20, Justify.Center);
```

See: Align Widget
