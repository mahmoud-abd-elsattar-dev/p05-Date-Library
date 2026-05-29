# 📅 Date Library

A comprehensive C++ date utility class that provides a wide range of static and instance methods for date manipulation, calculation, comparison, and calendar display.

---

## 📖 Overview

`clsDate` is a reusable C++ class that encapsulates a date (Day, Month, Year) and provides powerful utility methods for working with dates. It depends on `clsString` for string parsing. Every method is available in both a **static form** (works on any date) and an **instance form** (works on the object's internal value).

---

## ✨ Features

- **Multiple Constructors**: Create a date from today, a string (`"DD/MM/YYYY"`), separate values, or a day order in a year
- **Date Validation**: Check if a date is valid including leap year and month-day rules
- **Leap Year Detection**: Accurately determines leap years
- **Day & Month Info**: Get the number of days/hours/minutes/seconds in a month or year
- **Day of Week**: Get the day name or index for any date using Zeller's formula
- **Calendar Printing**: Print a formatted monthly or full yearly calendar
- **Date Arithmetic**: Add or subtract days, weeks, months, years, decades, centuries, and millennia
- **Date Comparison**: Check if a date is before, equal to, or after another date
- **Date Difference**: Calculate the number of days between two dates
- **Business Days**: Calculate business days, vacation days, and vacation return date
- **End Checks**: Check if a date is the last day of the week, month, or year
- **Age Calculator**: Calculate age in days from a date of birth

---

## 🚀 How to Use

Include the header files in your project:

```cpp
#include "clsDate.h"
```

### Instance Usage
```cpp
clsDate D(15, 6, 2024);

cout << D.DateToString();       // "15/6/2024"
cout << D.DayShortName();       // "Sat"
cout << D.isLeapYear();         // false
D.AddOneDay();
D.IncreaseDateByXMonths(3);
```

### Static Usage
```cpp
clsDate today = clsDate::GetSystemDate();
cout << clsDate::isLeapYear(2024);           // true
cout << clsDate::NumberOfDaysInAMonth(2, 2024); // 29

int diff = clsDate::GetDifferenceInDays(
    clsDate(1, 1, 2024),
    clsDate(1, 6, 2024)
);

clsDate::PrintMonthCalendar(6, 2024);
clsDate::PrintYearCalendar(2024);
```

---

## 🧠 Concepts Used

- **OOP** — Encapsulation of date data and behavior inside a class
- **Multiple Constructors** — Overloaded constructors for flexible object creation
- **Static Methods** — Utility functions callable without creating an instance
- **Properties** — Using `__declspec(property)` for clean Day/Month/Year get/set access
- **Enums** — `enDateCompare` (Before, Equal, After) and `enWhatToCount` for readable comparisons
- **Pass by Reference** — Modifying date objects directly inside arithmetic functions
- **Recursion & Loops** — Used in date arithmetic and difference calculations
- **Method Overloading** — Each method has both a static and an instance version
- **Dependency** — Uses `clsString` for parsing string-formatted dates
- **Time Library** — Uses `<ctime>` to retrieve the current system date

---

## 🔑 Key Methods

| Method | Description |
|---|---|
| `GetSystemDate()` | Returns today's date from the system clock |
| `IsValidDate()` | Validates a date including leap year rules |
| `DateToString()` | Converts a date to `"DD/MM/YYYY"` format |
| `isLeapYear()` | Checks if a year is a leap year |
| `NumberOfDaysInAMonth()` | Returns the number of days in a given month |
| `NumberOfDaysInAYear()` | Returns 365 or 366 based on leap year |
| `DayOfWeekOrder()` | Returns the day index (0=Sun … 6=Sat) using Zeller's formula |
| `DayShortName()` | Returns the short name of the day (Sun, Mon, …) |
| `MonthShortName()` | Returns the short name of the month (Jan, Feb, …) |
| `PrintMonthCalendar()` | Prints a formatted calendar for a given month |
| `PrintYearCalendar()` | Prints a full 12-month calendar for a given year |
| `AddOneDay()` | Increments the date by one day with month/year rollover |
| `IncreaseDateByXDays()` | Increases a date by a given number of days |
| `IncreaseDateByXWeeks()` | Increases a date by a given number of weeks |
| `IncreaseDateByXMonths()` | Increases a date by a given number of months |
| `IncreaseDateByXYears()` | Increases a date by a given number of years |
| `DecreaseDateByOneDay()` | Decrements the date by one day with month/year rollover |
| `GetDifferenceInDays()` | Returns the number of days between two dates |
| `IsDate1BeforeDate2()` | Checks if one date comes before another |
| `IsDate1EqualDate2()` | Checks if two dates are equal |
| `CompareDates()` | Returns Before, Equal, or After enum value |
| `IsWeekEnd()` | Checks if a date falls on Friday or Saturday |
| `IsBusinessDay()` | Checks if a date is a working day |
| `CalculateBusinessDays()` | Counts business days between two dates |
| `CalculateVacationReturnDate()` | Calculates the return date after a vacation |
| `CalculateMyAgeInDays()` | Returns age in days from a date of birth |
| `DaysUntilTheEndOfMonth()` | Returns remaining days until end of month |
| `DaysUntilTheEndOfYear()` | Returns remaining days until end of year |

---

## 📄 License

This project is open source and free to use for educational purposes.

---

## 👤 Author

👤 **Mahmoud Abd El-Sattar**  
📧 mahmoud.abdelsattar.dev@gmail.com  
💼 [linkedin.com/in/mahmoud-abd-el-sattar](https://www.linkedin.com/in/mahmoud-abd-el-sattar-1b227522a)
