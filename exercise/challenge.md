# Section 1: Pop Quiz (10 minutes)

A series of terms will be presented to you, and for each term you will be given
 60 seconds to write a brief response explaining the meaning or significance of
 the term.

For example you might be prompted HTML, and your description might be: markup
 language for rendering a web page

Do not worry if you come across a term you are unfamiliar with. For unfamiliar
 terms, feel free to use word association. For example, if you are prompted
 MySQL, you can write some data storage

# Section 2: Coding Challenge (50 minutes)

The challenge can be taken in your local environment or an online editor.

Implement a Calendar class which supports two operations:

1. Schedule events
2. Find time windows which are overbooked and find the associated conflicted events.

### Instructions

Please implement `Schedule` and `FindConflictedTimeWindows`. The return value
 of `FindConflictedTimeWindows` should be a list of `ConflictedTimeWindow`
 objects ordered by their start_time from earliest to latest. Please be aware
 that each `ConflictedTimeWindow` should contain ALL the conflicted events
 within the associated time period.

For example,

```C++
 Calendar calendar = Calendar()
 calendar.Schedule(new Event(4, "2014-01-02 10:00", "2014-01-02 11:00"))
 calendar.Schedule(new Event(5, "2014-01-02 09:30", "2014-01-02 11:30"))
 calendar.Schedule(new Event(6, "2014-01-02 08:30", "2014-01-02 12:30"))
 
 calendar.FindConflictedTimeWindows()
 // should return something like the following
 // [ConflictedTimeWindow("2014-01-02 09:30", "2014-01-02 10:00", { 5, 6 }),
 //  ConflictedTimeWindow("2014-01-02 10:00", "2014-01-02 11:00", { 4, 5, 6 }),
 //  ConflictedTimeWindow("2014-01-02 11:00", "2014-01-02 11:30", { 5, 6 }]
```