# MMM-CountDown
![Screenshot_1](https://github.com/bikerpatch/MMM-CountDown/raw/master/Screenshot_1.png)

This is a module for the [MagicMirror²](https://github.com/MichMich/MagicMirror/) which can count down the days to a date/event.

## Using the module

To use this module, add the following configuration block to the modules array in the `config/config.js` file:

```js
var config = {
    modules: [
        {
            module: 'MMM-CountDown',
            config: {
                // See configuration options
            }
        }
    ]
}
```

## Configuration options

| Option           | Description                                                                                                           |
| ---------------- | --------------------------------------------------------------------------------------------------------------------- |
| `event`          | *Required* Name of event to count down to (displayed above counter)                                                   |
| `date`           | *Required* Date to count down to (YYYY-MM-DD HH:MM:SS+00:00)                                                          |
| `eventDataUrl`   | Full URL of the iCal calendar to use to load events.  Will count down to the start of the next event                  |
| `reloadInterval` | Interval to use to refresh events from the eventDataUrl                                                               |
| `showHours`      | Decide whether or not to display the hours. Default is true                                                           |
| `showMinutes`    | Decide whether or not to display the minutes. Default is true                                                         |
| `showSeconds`    | Decide whether or not to display the seconds. Default is true                                                         |
| `customInterval` | Change the UI refresh update interval which will help reduce load if you are only showing specific time metrics. Default is 1000 |
| `daysLabel`      | Choose how you wish to display your Days label. Default is Days                                                       |
| `hoursLabel`     | Choose how you wish to display your Hours label. Default is Hours                                                     |
| `minutesLabel`   | Choose how you wish to display your Minutes label. Default is Minutes                                                 |
| `secondsLabel`   | Choose how you wish to display your Seconds label. Default is Seconds                                                 |
| `debug`          | Enable debugging.  Default is false                                                                                   |

If either of the above are missing, or the iCal URL doesn't have any future events, the module will count down to the New Millenium (3000-01-01).

Note: does not support repeating iCal events
