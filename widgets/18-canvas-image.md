# CanvasImage Widget

The CanvasImage widget displays image files in the console.

## Basic Usage

```csharp
AnsiConsole.Write(new CanvasImage("image.png"));
```

## Max Width

```csharp
new CanvasImage("photo.jpg").MaxWidth(80);
```

## Pixel art mode

```csharp
new CanvasImage("pixel.png").PixelArtMode();
```

## Style

```csharp
new CanvasImage("image.png")
    .Style(new Style(Color.White, Color.Black));
```

## Rounded

```csharp
new CanvasImage("image.png").Rounded();
```

Supported formats: PNG, JPG, BMP, GIF

See: Canvas Widget
