# BreakdownChart Widget

The BreakdownChart widget displays proportional data as colored bar charts.

## Basic Usage

```csharp
AnsiConsole.Write(new BreakdownChart()
    .AddItem("Used", 75, Color.Red)
    .AddItem("Free", 25, Color.Green));
```

## Width

```csharp
new BreakdownChart().Width(40);
```

## Show Percentage

```csharp
new BreakdownChart().ShowPercentage();
```

## Full Example

```csharp
new BreakdownChart()
    .Width(50)
    .ShowPercentage()
    .AddItem("Memory", 8, Color.Blue)
    .AddItem("Free", 8, Color.Green);
```

See: BarChart Widget
