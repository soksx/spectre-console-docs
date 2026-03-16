# Status Display

Show animated status indicators with spinners.

## Basic Usage

```csharp
AnsiConsole.Status()
    .Start("Processing...", ctx =>
    {
        // Do work
        Thread.Sleep(1000);
    });
```

## Spinner Style

```csharp
AnsiConsole.Status()
    .Spinner(Spinner.Known.Dots)
    .Start("Loading...");
```

## Update Status

```csharp
ctx.Status("Step 1...");
Thread.Sleep(500);
ctx.Status("Step 2...");
```

See: Progress Display
