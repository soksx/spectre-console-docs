# Show Progress Bars

Display progress bars for long-running operations.

## Basic Usage

```csharp
AnsiConsole.Progress()
    .Start(ctx =>
    {
        var task = ctx.AddTask("Downloading");
        while (!task.IsFinished)
        {
            task.Increment(1);
            Thread.Sleep(50);
        }
    });
```

## Multiple Tasks

```csharp
var file1 = ctx.AddTask("File 1", maxValue: 100);
var file2 = ctx.AddTask("File 2", maxValue: 50);
```

## Columns

```csharp
.Columns(
    new SpinnerColumn(),
    new TaskDescriptionColumn(),
    new ProgressBarColumn(),
    new PercentageColumn()
)
```

## Styling

```csharp
new ProgressBarColumn
{
    CompletedStyle = new Style(Color.Green),
    RemainingStyle = new Style(Color.Grey)
}
```

See: Status Display, Live Display
