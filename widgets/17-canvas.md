# Canvas Widget

The Canvas widget draws pixel-level graphics in the console.

## Basic Usage

```csharp
var canvas = new Canvas(80, 24);

for (int x = 0; x < 80; x++)
{
    for (int y = 0; y < 24; y++)
    {
        canvas.SetPixel(x, y, Color.Red);
    }
}

AnsiConsole.Write(canvas);
```

## Set Pixel

```csharp
canvas.SetPixel(x, y, Color.Blue);
canvas.SetPixel(x, y, Color.Green, Color.White);
```

## Draw Shapes

```csharp
canvas.DrawCircle(40, 12, 10, Color.Red);
canvas.DrawRectangle(10, 5, 30, 15, Color.Blue);
```

## Fill

```csharp
canvas.Fill(Color.White);
```

See: CanvasImage Widget
