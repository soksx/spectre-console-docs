# Rule Widget

The Rule widget creates horizontal dividers and section separators with optional titles.

## Basic Usage

```csharp
AnsiConsole.Write(new Rule("Section Title"));
AnsiConsole.Write(new Rule());
```

## With Style

```csharp
new Rule("[yellow]Warning[/]")
    .RuleStyle(Style.Parse("red bold"));
```

## Border Style

```csharp
new Rule().Border(BoxBorder.Rounded);
new Rule().Border(BoxBorder.Heavy);
```

## Justification

```csharp
new Rule("Title").Justification(Justify.Left);
new Rule("Title").Justification(Justify.Center);
new Rule("Title").Justification(Justify.Right);
```

## Full Example

```csharp
AnsiConsole.Write(new Rule("[bold yellow]Header Section[/]")
    .RuleStyle(Style.Parse("green"))
    .Justification(Justify.Center));
```

See: Panel Widget
