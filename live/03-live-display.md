# Live Display

Update and refresh any renderable content dynamically in real-time.

## Basic Usage

```csharp
AnsiConsole.Live(new Markup("Loading..."))
    .Start(l =>
    {
        l.Update(new Markup("Step 1..."));
        Thread.Sleep(500);
        l.Update(new Markup("Done!"));
    });
```

## With Progress

```csharp
var progress = new ProgressBar();
AnsiConsole.Live(progress).Start(l =>
{
    for (int i = 0; i <= 100; i += 10)
    {
        progress.Value = i;
        l.Refresh();
        Thread.Sleep(100);
    }
});
```

See: Progress Display, Status Display
