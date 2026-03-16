# Test Console Output

Write unit tests for console applications using TestConsole.

## Basic Usage

```csharp
var console = new TestConsole();
console.Write(new Markup("[green]Success[/]"));
Assert.Contains("Success", console.Output);
```

## Capture Output

```csharp
var console = new Test profiler = new TestConsole();
console.WriteLine("Hello");

var output = console.Output;
Assert.Contains("Hello", output);
```

## With Ansi Codes

```csharp
console.Write(new Markup("[red]Error[/]"));
// Test with or without ANSI
Assert.True(console.Output.Contains("\x1b[31m"));
```

## Interactive Tests

```csharp
console.Input.PushText("John");
var name = console.Ask<string>("Name?");
Assert.Equal("John", name);
```

See: AnsiConsole Testing
