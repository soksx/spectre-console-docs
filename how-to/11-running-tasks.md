# Run Tasks with Spinner

Show spinner animation while awaiting async operations.

## Basic

```csharp
AnsiConsole.Status()
    .Start("Loading...", async ctx =>
    {
        await Task.Delay(1000);
    });
```

## Async with Update

```csharp
AnsiConsole.Status()
    .Start(async ctx =>
    {
        ctx.Status("Fetching data...");
        var data = await FetchAsync();
        
        ctx.Status("Processing...");
        await ProcessAsync(data);
    });
```

## Spinner Style

```csharp
.Spinner(Spinner.Known.Dots)
.SpinnerStyle(Style.Parse("green"))
```

See: Status Display
