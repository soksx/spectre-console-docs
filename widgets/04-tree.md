# Tree Widget

The Tree widget displays hierarchical data structures with expandable tree views.

## Basic Usage

```csharp
var tree = new Tree("Root");

var child1 = tree.AddNode("Child 1");
child1.AddNode("Grandchild 1.1");
child1.AddNode("Grandchild 1.2");

var child2 = tree.AddNode("Child 2");

AnsiConsole.Write(tree);
```

## Tree Guide Styles

```csharp
tree.Guide(TreeGuide.DoubleLine);
tree.Guide(TreeGuide.Box);
tree.Guide(TreeGuide.Ascii);
tree.Guide(TreeGuide.None);
```

## Node Methods

```csharp
var node = tree.AddNode("Name");
node.AddNode("Child");
node.AddNodes("A", "B", "C");
node.Collapse();
node.Expand();
```

## Collapse/Expand

```csharp
tree.CollapseAll();
tree.ExpandAll();
```

See: Columns Widget, Grid Widget
