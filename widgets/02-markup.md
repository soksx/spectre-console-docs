# Markup Widget

The Markup widget renders text with colors and decorations using inline tag syntax like `[bold red]text[/]`.

## Basic Usage

```csharp
AnsiConsole.MarkupLine("[green]Success![/]");
AnsiConsole.MarkupLine("[red]Error[/]");
AnsiConsole.MarkupLine("[blue]Info:[/] Processing...");
```

## Colors

```csharp
[green]Green[/]
[red]Red[/]
[blue on yellow]Blue on Yellow[/]
```

## Styles

```csharp
[bold]Bold[/]
[italic]Italic[/]
[underline]Underlined[/]
[bold red]Bold Red[/]
```

## Escaping

```csharp
Markup.Escape("User [input]")  // Escape brackets
Markup.Remove(styledText)       // Remove markup
```

See: Text Widget, Color Reference
