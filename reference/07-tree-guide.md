# Tree Guide Reference

All tree guide styles for tree views.

## Available Guides

| Style | Example |
|-------|----------|
| None | No guide lines |
| ASCII | | +-- |
| ASCII2 | | +-+ |
| Bold | ┃ ┣┫ |
| Box | │ ├── └── |
| DoubleBox | ║ ╠╬╣ |
| Round | │ ├─└ |

## Usage

```csharp
tree.Guide(TreeGuide.Box);
tree.Guide(TreeGuide.DoubleLine);
```

## Custom

Custom tree guides available in advanced usage.
