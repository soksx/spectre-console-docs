# Update Content Live

Update console output in-place without scrolling.

## AnsiConsole.Live()

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
    for(int i=0; i<=100; i+=10)
    {
        progress.Value = i;
        l.Refresh();
        Thread.Sleep(100);
    }
});
```

## Stop

```csharp
l.Stop();  // Stop live display
```

See: Live Display
