# Show Activity Status

Display a spinner for operations without measurable progress.

## Basic Usage

```csharp
AnsiConsole.Status()
    .Start("Loading...", ctx =>
    {
        Thread.Sleep(2000);
    });
```

## Custom Spinner

```csharp
AnsiConsole.Status()
    .Spinner(Spinner.Known.Dots)
    .Start("Processing...");
```

## Update Status

```csharp
ctx.Status("Step 1...");
Thread.Sleep(500);
ctx.Status("Step 2...");
```

See: Progress Display
