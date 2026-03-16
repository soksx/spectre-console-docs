# Showing Status and Spinners

In this tutorial, we'll build a coffee brewing simulation that shows animated spinners while work happens. By the end, you'll know how to display status messages, update them as work progresses, and customize the spinner style.

## 1. Show a Basic Spinner

Let's start by showing a spinner while our "coffee grinder" runs. The `Status()` method displays an animated spinner with a message:

```csharp
AnsiConsole.Status()
    .Start("Grinding beans...", ctx =>
    {
        // Simulate grinding
        Thread.Sleep(3000);
    });

AnsiConsole.MarkupLine("[green]Done![/]");
```

Run the code:
```bash
dotnet run
```

An animated spinner appears next to "Grinding beans..." that runs for a few seconds, then "Done!" appears.

The spinner animates automatically - Spectre.Console handles the animation loop for you. Just put your work inside the callback.

Your first status spinner.

## 2. Update the Status Text

Real tasks have multiple stages. Let's update the status message as our coffee progresses through grinding, brewing, and pouring:

```csharp
AnsiConsole.Status()
    .Start("Grinding beans...", ctx =>
    {
        Thread.Sleep(1500);

        ctx.Status("Brewing coffee...");
        Thread.Sleep(2000);

        ctx.Status("Pouring into cup...");
        Thread.Sleep(1000);
    });

AnsiConsole.MarkupLine("[green]Coffee is ready![/]");
```

Run it:
```bash
dotnet run
```

The message changes from "Grinding beans..." to "Brewing coffee..." to "Pouring into cup..." - all while the spinner keeps animating.

We use `ctx.Status()` to change the message. The ctx parameter gives you control over the status display while it's running.

Your status now reflects what's actually happening.

## 3. Try Different Spinners

Spectre.Console includes many spinner styles. Let's try a few to see the difference:

```csharp
// Calm and steady
AnsiConsole.Status()
    .Spinner(Spinner.Known.Dots)
    .Start("Grinding beans...", ctx =>
    {
        Thread.Sleep(2000);
    });

// Energetic
AnsiConsole.Status()
    .Spinner(Spinner.Known.Star)
    .SpinnerStyle(Style.Parse("yellow"))
    .Start("Brewing coffee...", ctx =>
    {
        Thread.Sleep(2000);
    });

AnsiConsole.MarkupLine("[green]Done![/]");
```

Run it:
```bash
dotnet run
```

Two different spinner animations appear - the smooth Dots spinner for grinding, then the lively Star spinner (in yellow) for brewing.

`.Spinner()` sets the animation style while `.SpinnerStyle()` sets the color. Match the spinner to your app's personality.

You can now customize the look and feel of your spinners.

## 4. Complete Coffee Brew

Let's put it all together into a complete brewing experience that changes both the message and spinner style at each stage:

```csharp
AnsiConsole.MarkupLine("[bold yellow]Time for coffee![/]");
AnsiConsole.WriteLine();

AnsiConsole.Status()
    .Spinner(Spinner.Known.Dots)
    .SpinnerStyle(Style.Parse("yellow"))
    .Start("Grinding beans...", ctx =>
    {
        Thread.Sleep(2000);

        ctx.Spinner(Spinner.Known.Star);
        ctx.SpinnerStyle(Style.Parse("blue"));
        ctx.Status("Brewing coffee...");
        Thread.Sleep(2500);

        ctx.Spinner(Spinner.Known.Arc);
        ctx.SpinnerStyle(Style.Parse("green"));
        ctx.Status("Pouring into cup...");
        Thread.Sleep(1500);
    });

AnsiConsole.WriteLine();
AnsiConsole.MarkupLine("[green]Your coffee is ready! Enjoy![/]");
```

Run the complete application:
```bash
dotnet run
```

"Time for coffee!" appears, followed by an animated brewing sequence: yellow dots while grinding, blue stars while brewing, and a green arc while pouring - then the final success message.

Both spinner and color change using `ctx.Spinner()` and `ctx.SpinnerStyle()`, creating a dynamic, engaging experience.

A polished status display with some personality.

---

## Summary

You've created a coffee brewing simulation that demonstrates all the core status features. Your application shows animated spinners, updates messages as work progresses, and customizes the spinner style to match each stage.

Add these spinners to file uploads, API calls, database queries, build processes - anywhere users wait for work to complete.
