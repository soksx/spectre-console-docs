# Organize Layout

Arrange content using panels, columns, grids, and alignment.

## Panel

```csharp
new Panel("Content")
    .Header("Title")
    .Border(BoxBorder.Rounded);
```

## Grid

```csharp
new Grid()
    .AddColumn()
    .AddRow("Col1", "Col2");
```

## Columns

```csharp
new Columns("Left", "Right");
```

## Layout

```csharp
new Layout("Root")
    .SplitRows(
        new Layout("Header"),
        new Layout("Main")
    );
```

See: Grid Widget, Panel Widget
