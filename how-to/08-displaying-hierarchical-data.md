# Display Hierarchical Data

Visualize nested structures using tree views with customizable styling.

## Tree Widget

```csharp
var tree = new Tree("Root");
var child = tree.AddNode("Child");
child.AddNode("Grandchild");
AnsiConsole.Write(tree);
```

## Tree Guide Styles

```csharp
tree.Guide(TreeGuide.DoubleLine);
tree.Guide(TreeGuide.Box);
tree.Guide(TreeGuide.Ascii);
```

## Tree Node Methods

```csharp
node.AddNode("Name");
node.AddNodes("A", "B", "C");
nodeCollapse();
node.Expand();
```

See: Tree Widget
