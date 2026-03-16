# Calendar Widget

The Calendar widget displays monthly calendars with highlighted dates.

## Basic Usage

```csharp
AnsiConsole.Write(new Calendar(2024, 1));
```

## Highlight Dates

```csharp
var calendar = new Calendar(2024, 1);
calendar.AddHolidays(new DateTime(2024, 1, 1));
calendar.Highlight(new DateTime(2024, 1, 15), Color.Red);
```

## Style

```csharp
calendar.HeaderStyle(new Style(Color.Blue));
calendar.DayStyle(new Style(Color.White));
```

## Culture

```csharp
new Calendar(2024, 1, new CultureInfo("es-ES"));
```

See: DateTime
