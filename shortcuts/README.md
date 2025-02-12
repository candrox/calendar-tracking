# Calendar Tracking (Shortcuts)

## What are shortcuts? 
Apple shortcuts are small programs that can be created by connecting simple action blocks. The below collection of shortcuts are used to create and update calendar events.

Note: In order to automatically allow updating of calendar events in your calendar without manual user confirmation each time, configure the following:
- iOS: Open the iOS 'Settings' app, go to 'Shortcuts' -> 'Advanced' and activate 'Allow Deleting Without Confirmation'. 
- macOS: Open the macOS Shortcuts, go to 'Preferences' -> 'Advanced' and activate 'Allow Deleting Without Confirmation'.
<br />
<br />

## Downloads
In 'Edit' mode, the below shortcuts have a 'Settings' section at the top each shortcut which allows for configuration and customisation. A description of all settings can be found further down below.

<div align="center">

|Shortcut|Description|
|:-                                                                                      |:-           |
|[FOO - Meal](https://www.icloud.com/shortcuts/792fbe1a035c4231a7a89173e0c44b19)         |Food - logs Breakfast, Lunch, Dinner |
|[RES - Sleep](https://www.icloud.com/shortcuts/b909328d5cce4c38bcab99d94396b612)        |Rest - asks your Sleep & Drowse times |
|[ERR - Shopping](https://www.icloud.com/shortcuts/d8b6d55ffe0146adbd26ebd23a5962ad)     |Errands - logs shopping activity|
|[TRA - Walk](https://www.icloud.com/shortcuts/a182ea15d56f4f9493d37f46c0e0ed93)         |Transportation - logs a walk|
|[TRA - Car](https://www.icloud.com/shortcuts/618a22e19144425681ff7c5d7b1bf2ba)          |Transportation - logs a car ride|
|[TRA - Bus](https://www.icloud.com/shortcuts/eedbb943135745b0bdeeaa8c09fd0f95)          |Transportation - logs a bus ride|
|[TRA - Taxi](https://www.icloud.com/shortcuts/d2b2c0be68af41119cd701136b156f53)         |Transportation - logs a taxi ride| 
|[TRA - Subway](https://www.icloud.com/shortcuts/818c30f91a68425b897a567ceaf59c7e)       |Transportation - logs a subway ride|
|[HYG - Personal](https://www.icloud.com/shortcuts/601083e57e1640a6bf9d5d1899be549a)     |Hygiene - logs personal bathroom time|
|[HYG - Shower](https://www.icloud.com/shortcuts/f40e55c060af4fa58d2adb3d3b210d4a)       |Hygiene - logs a shower|
|[HYG - Toilet](https://www.icloud.com/shortcuts/b9914c3e2b3b4648bc7ca8eea67ae615)       |Hygiene - logs toilet time|
|[HYG - Haircut](https://www.icloud.com/shortcuts/e7189da916b540c8836a9fcc69efb6d8)      |Hygiene - logs a haircut|
|[Connect](https://www.icloud.com/shortcuts/96dee8d7f3b94da48b530aff56dcb4c9)            |Connects the last two calendar events by setting the end time of the first event to <br>the start time of the second event. This is useful to connect two events by removing <br>the time gap in between. |
|[Stop Event Now](https://www.icloud.com/shortcuts/31552dfb24774a1686f956e695ac9032)     |Moves the end time of a selected event to the nearest X minute from now|
|[Move Event Earlier](https://www.icloud.com/shortcuts/6f1466e97e654e3b8cbbfbc376dd1b4d) |Shifts a selected event to X minutes earlier by updating the event start and end time|
|[Move Event Later](https://www.icloud.com/shortcuts/55bc65bd5be149f1a184cd5fb4841185)   |Shifts a selected event to X minutes later by updating the event start and end time|
|[Backup & Restore](https://www.icloud.com/shortcuts/bd469c0b7f36476baeeb6f6ffae165a3)   |Saves and restores your shortcuts collection|
</div>  
<br />
<br />

## Configuration
The shortcuts offer a variety of configuration options which can be found atop each shortcut in the 'Settings' section.
<br />

**Shortcuts :: versionNumber**  
Documents the shortcut version number in YYYYMMDD format. Technically this can be any text.
* 20201031
* 20210606
* ...
<br />

**Shortcuts :: eventCalendar**  
Specifies the calendar name the event should be logged in.
* Work
* Home
* ...
<br />

**Shortcuts :: eventTitle**  
Specifies the event title.
* Meeting with Godzilla
* 99th Birthday Anniversary
* ...
<br />

**Shortcuts :: eventLocation**  
Specifies the event location.
* Baseball Stadium Staines
* 1 Main Street, City 2345, Country
* ...
<br />

**Shortcuts :: eventNote**  
Specifies event notes.
* Try to take over the world
* Buy more milk and more cheese
* ...
<br />

**Shortcuts :: eventRoundMinute**  
Rounds the event start time up or down to the nearest specified minute. As an example, if the 'eventRoundMinute' is set to '5' minutes a shortcut that is run at 11:22:35 will be rounded up to 11:25:00. A shortcut that is run at 11:22:25 will be rounded down to 11:20:00. Setting can not be '0'.
* 1
* 5
* ...
<br />

**Shortcuts :: eventDuration**  
Specifies the default event duration in minutes. As an example, if the 'eventDuration' is set to '5' minutes an new created event with start time of 11:25:00 will have the end time automatically set to 11:30:00.
* 1
* 5
* ...
<br />

**Shortcuts :: eventExtension**  
Specifies the event extension in minutes. When a shortcut (to create a new event) is run, it will check if the same type of event already exists, and if so, will remove the existing event and replace it with a new event by using the original start time but extending the end time by adding the 'eventExtension' minutes. This function allows to quickly update the duration of an existing event by simply running the same event multiple times in succession. This functionality ties in with the 'eventSearchMinusTime' and 'eventSearchPlusTime' for a more personalised setup.
* 1
* 5
* ...
<br />

**Shortcuts :: eventSearchMinusTime**  
Specifies the amount of minutes the search should look back in time from now to find the same type of event. This setting ties in with the 'eventExtension'. Set to '0' if existing events should not be touched and a brand-new event should be created instead.
* 1
* 5
* ...
<br />

**Shortcuts :: eventSearchPlusTime**  
Specifies the amount of minutes the search function should look forward in time from now to find the same type of event. This setting ties in with the 'eventExtension'. Set to '0' if existing events should not be touched and a brand-new event should be created instead.
* 5
* 10
* ...
<br />

**Shortcuts :: acousticFeedbackVoice**  
Specifies text the device says when the shortcut is run. By default this is set with an empty space character to mute any notification.
* Woohoo!
* Shortcut run successfully!
* ...
<br />

**Shortcuts :: acousticFeedbackFile**  
Specifies an audio file used for devices without vibration functionality to indicate if an event was rounded up or down based on the 'eventRoundMinute' setting. The audio file will be played once if an event start time was rounded down, and will play twice if an event start time was rounded up.
* file:///System/Library/Audio/UISound/begin_record.caf
* http://awesomesounds.com/IceCream/Scream.aaf
* ...
<br />

**Shortcuts :: acousticFeedbackVolume**  
Specifies the volume level at which acoustic feedback is played. The shortcut retains the original system volume level and only temporary changes the output volume to provide feedback.
* 0.1
* 0.9
* ...
<br />
<br />
