# Draw Charts

Visualize data with bar charts, breakdown charts, and calendars.

## BarChart

```csharp
AnsiConsole.Write(new BarChart()
    .AddItem("Q1", 100, Color.Blue)
    .AddItem("Q2", 150, Color.Green));
```

## BreakdownChart

```csharp
AnsiConsole.Write(new BreakdownChart()
    .AddItem("Used", 75, Color.Red)
    .AddItem("Free", 25, Color.Green));
```

## Calendar

```csharp
AnsiConsole.Write(new Calendar(2024, 1));
```

## Style

```csharp
new BarChart().Width(40).ShowValues();
```

See: BarChart Widget, BreakdownChart Widget
