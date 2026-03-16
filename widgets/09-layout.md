# Layout Widget

The Layout widget creates complex multi-section layouts.

## Basic Usage

```csharp
var layout = new Layout("Root")
    .SplitRows(
        new Layout("Header"),
        new Layout("Main"),
        new Layout("Footer")
    );
```

## Split Columns

```csharp
layout.SplitColumns(
    new Layout("Left"),
    new Layout("Right")
);
```

## Size

```csharp
new Layout("Name").Size(20);
layout["Left"].Ratio(1);
layout["Right"].Ratio(2);
```

See: Grid, Panel
