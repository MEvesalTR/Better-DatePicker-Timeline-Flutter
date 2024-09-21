# BetterDatePickerTimeline

[![Pub](https://img.shields.io/pub/v/better_date_picker_timeline?color=%232bb6f6)](https://pub.dev/packages/better_date_picker_timeline)

<p>
 <img src="https://github.com/MEvesalTR/Better-DatePicker-Timeline-Flutter/blob/dev/screenshots/demo.gif?raw=true"/>
</p>

## 🎨 Why BetterDatePickerTimeline?

The `better_date_picker_timeline` package is an enhanced version of the [`date_picker_timeline`](https://pub.dev/packages/date_picker_timeline) package. It offers more customization options to better suit your needs.

#### New Features

- **[Added] scrollDirection**: Allows the user to specify the axis of the date picker, whether horizontal or vertical.

- **[Added] physics**: Adding this parameter enhances the user experience when interacting with the ListView.

- **[Added] padding**: Users can now add padding to the first and last elements of the ListView from the sides.

- **[Replaced] decoration**: This parameter replaces `selectionColor`, allowing for more customization of the background.

- **[Fixed] deactivatedTextColor**: Fixed the naming of this parameter.

## 🚩 Calendar Support (Gregorian & Jalali)

With the `calendarType` parameter, users can switch between the default Gregorian calendar and the Jalali (Persian) calendar by setting it to `CalendarType.persianDate`.


## 🧩 How To Use

Import the following package in your dart file

```dart
import 'package:better_date_picker_timeline/date_picker_timeline.dart';
```

## ⚙️ Usage

This version is breaking backwards compatibility

Use the `DatePicker` Widget

```dart
Column(
    mainAxisAlignment: MainAxisAlignment.center,
    children: [
      DatePicker(
        DateTime.now(),
        initialSelectedDate: DateTime.now(),
        selectedTextColor: Colors.white,
        onDateChange: (date) {
          // New date selected
          setState(() {
            _selectedValue = date;
          });
        },
      ),
    ],
)
```

#### Constructor:

```dart
DatePicker(
    this.startDate, {
    Key key,
    this.width,
    this.height,
    this.controller,
    this.scrollDirection = Axis.horizontal,
    this.physics,
    this.padding,
    this.monthTextStyle,
    this.dayTextStyle,
    this.dateTextStyle,
    this.selectedTextColor,
    this.decoration,
    this.deactivatedTextColor,
    this.initialSelectedDate,
    this.activeDates,
    this.inactiveDates,
    this.daysCount,
    this.onDateChange,
    this.locale = "en_US",
    this.calendarType = CalendarType.gregorianDate,
    this.directionality,
}) : super(key: key);
```