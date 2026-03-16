# BarChart Widget

The BarChart widget visualizes numeric data as horizontal bars.

## Basic Usage

```csharp
AnsiConsole.Write(new BarChart()
    .AddItem("Q1", 100, Color.Blue)
    .AddItem("Q2", 150, Color.Green));
```

## Width

```csharp
new BarChart().Width(40);
```

## Show Values

```csharp
new BarChart().ShowValues();
```

## Max Value

```csharp
new BarChart().WithMaxValue(200);
```

See: BreakdownChart
