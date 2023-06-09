# DayPilot Lite for JavaScript

[DayPilot Lite for JavaScript](https://javascript.daypilot.org/open-source/) is a library of JavaScript/HTML5 event calendar/scheduler components that can display day/week/month calendar views.

## What's New

[Release History](https://javascript.daypilot.org/daypilot-lite-history/)

## Online Demo

[![JavaScript Event Calendar Demo](https://static.daypilot.org/npm/202207/javascript-html5-event-calendar-scheduler-drag-drop.png)](https://javascript.daypilot.org/demo/lite/)

[Online Demo](https://javascript.daypilot.org/demo/lite/)

## Features

* Calendar/scheduler views: day, week, work week, month, resource calendar
* Event creation using drag and drop
* Drag and drop event moving and resizing
* Integrated delete icon
* Event duration bar with customizable color
* Date picker with free/busy days highlighting, free-hand range selection, day cell customization
* CSS themes (use theme builder to create your own theme)
* Event customization (text, HTML, colors...)
* Built-in XSS protection
* Localization support
* TypeScript definitions

## Tutorials

### JavaScript Event Calendar Tutorial

[![JavaScript/HTML5 Event Calendar](https://static.daypilot.org/npm/202207/javascript-html5-event-calendar-scheduler-open-source.png)](https://code.daypilot.org/17910/html5-event-calendar-open-source)

[HTML5/JavaScript Event Calendar (Open-Source)](https://code.daypilot.org/17910/html5-event-calendar-open-source)  
Event calendar introduction - week view, loading data, drag and drop, CSS themes, sample PHP REST backend.

### JavaScript Resource Calendar Tutorial

[![JavaScript Resource Calendar](https://static.daypilot.org/npm/202207/javascript-resource-calendar-open-source.png)](https://code.daypilot.org/87709/javascript-resource-calendar-tutorial-php-mysql)

[JavaScript Resource Calendar Tutorial - PHP/MySQL (Open-Source)](https://code.daypilot.org/87709/javascript-resource-calendar-tutorial-php-mysql)  
The resource calendar displays custom resources (people, rooms, tools) as columns. This tutorial shows how to load resource data from a PHP/MySQL backend and show custom calendar columns.

## Example

HTML:

```html
<div id="calendar"></div>
<script src="app.js"></script>
```

JavaScript:

```javascript
import {DayPilot} from "@daypilot/daypilot-lite-javascript";

// initialize the calendar component
const calendar = new DayPilot.Calendar("calendar", {
    viewType: "Week",
    startDate: "2022-03-21",
    headerDateFormat: "d/M/yyyy",
    onEventMoved: args => {
        console.log("Event was moved:", args.e);
    }
});
calendar.init();

// load calendar events
const events = [
    {
        start: "2022-03-20T11:00:00",
        end: "2022-03-20T14:00:00",
        id: 1,
        text: "Event 1",
        barColor: "#f37021"
    },
    {
        start: "2022-03-21T11:00:00",
        end: "2022-03-21T14:00:00",
        id: 2,
        text: "Event 2",
        barColor: "#cc004c"
    }
];
calendar.update({events});
```

## Documentation

* [Weekly calendar](https://doc.daypilot.org/calendar/week-view/)
* [Monthly calendar](https://doc.daypilot.org/month/)
* [Resource calendar](https://doc.daypilot.org/calendar/resources-view/)
* [Date picker](https://doc.daypilot.org/navigator/)

## CSS Themes

The [Theme Designer](https://themes.daypilot.org/) lets you create and download your own CSS theme using an online visual tool.

## License

Apache License 2.0



