# MeridianPane support

MeridianPane is a free, offline world clock and meeting planner for macOS 14 or later. No account, advertisements, purchases, or subscription.

## Get started

Live clocks shows the current date and time in each location. Switch to Plan meeting to choose a local date and time in the reference zone. Use a location’s options menu to change the reference; this preserves the chosen instant. Next quarter hour selects the next quarter-hour boundary at or after now.

Add up to eight time zones by searching for a city, region, or identifier. The location menu also lets you rename, reorder, remove, or edit working hours. Undo removal restores the last removed location during the current session. At least one location is required.

## Working hours and shared times

Choose weekdays and whole-hour working times for each location. Equal start and end means 24 hours on the selected days. Overnight hours belong to the day the shift starts. No selected days means unavailable.

Find shared working times checks every 15-minute start on the reference date. The entire meeting must fit every location’s selected hours. A candidate may end on the next day. Duration is 15 minutes to 8 hours in 15-minute steps. These are configured working times, not actual calendar availability; holidays, appointments, and invitations are not checked.

Dates from 2020 through 2100 are supported. Times use the rules installed on your Mac. A skipped local time requires another time. A repeated local time requires choosing the desired UTC offset; exports remain disabled until resolved. When a meeting crosses midnight or an offset change, its card also displays the ending date and offset. Keep macOS updated for rule changes, and check important meeting details with participants.

## Copy and export

Copy summary writes the title, notes, duration, full local start/end dates, and time-zone identifiers to the clipboard. Export .ics creates a calendar file using absolute UTC start and end times. Import the file into your preferred calendar yourself. MeridianPane does not access calendars or send invitations. Each export creates a new event identifier, so importing repeated exports can create duplicate calendar events.

Exports require a new filename; existing files and links are never overwritten.

## Save and transfer setups

Locations, working hours, display preference, and the last valid meeting are automatically saved in MeridianPane’s local Application Support folder inside its macOS sandbox. Export setup creates a portable JSON file. Import setup validates a MeridianPane format version 1 file, then saves and backs up the current setup before replacing it. Setup files are limited to 100 KB, labels to 40 characters, titles to 120, and notes to 2,000.

Show local storage opens the storage folder in Finder, including backups. Backups can be restored through Import setup. Backups remain local until you manage them yourself. The app does not sync through an account or store credentials.

If saving fails, a visible warning offers retry and export. Closing or quitting warns when the session could not be saved. An unreadable saved setup is preserved; Back up & reset copies the unreadable file before creating defaults. Export any current session you want to keep before resetting. Unresolved edits to a skipped or repeated local time are not saved; the last valid meeting remains saved.

## Help

Open a [public support issue](https://github.com/valimikayilov/free-app-support/issues). Describe your macOS version, selected time zones, and the steps involved. Do not include private meeting notes or confidential setup files.

[Privacy policy](privacy.md)
