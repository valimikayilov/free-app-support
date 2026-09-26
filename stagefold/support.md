# Stagefold support

Stagefold is a free Mac agenda and presentation timer. The first release is in preparation.

## Run a rehearsal

1. Choose a sample agenda or create your own with the plus button.
2. Select each cue to edit its title, optional speaker, duration in seconds, warning threshold, and private presenter note.
3. Choose whether cues advance automatically at zero. With this option off, a cue counts overtime until you choose **Next cue**.
4. Choose **Start agenda**. Use **Pause/Resume**, **Next cue**, or the rehearsal actions menu to end the session.
5. Open **Stage display** for a separate window. Move it to the display you want and use its full-screen button or the standard macOS window control. Private notes and operator controls are not shown there.
6. Open **Rehearsals** to inspect completed or ended sessions and export CSV reports.

The keyboard shortcuts are Command–Shift–Space for start/pause, Command–Right Arrow for next cue, and Command–D for the stage display. These are app shortcuts, not system-wide hotkeys. The menu bar also offers basic controls.

## Time and interruptions

A running timer measures elapsed time with a monotonic clock and includes sleep time while the app remains open. Automatic agendas catch up to the correct cue after a delayed update or wake. A Mac cannot play timer sounds while asleep. Optional keep-awake and sound controls are off by default.

When you quit and reopen Stagefold, a saved session restores **paused at its last checkpoint**. Time while the app was closed is not added. Checkpoints are saved approximately once per second during a session and at control actions; an abrupt shutdown can lose the interval since the last successful save. The restoration banner makes this behavior explicit.

## Save and exchange plans

Plans, settings, and the latest 30 rehearsal reports are stored locally. Use **Export agenda** to save a Stagefold JSON file. **Import agenda** reads that format and adds a new independent copy; it does not replace an existing agenda. CSV exports include planned and actual cue durations, differences, and cues that were not reached.

The app supports up to 100 agendas, 200 cues per agenda, and cue durations of 1 second to 24 hours. Titles and speaker names are limited to 100 characters, notes to 4,000 characters, agenda imports to 2 MB, and the local library to 20 MB. These are stability limits; no purchase removes them.

If the saved library cannot be read, Stagefold preserves the original file and stops overwriting it. Export any new work before using **Back up & reset**. That action copies the existing file to a separate backup before creating a fresh sample library. **Show file** reveals the storage location in Finder.

## Scope and privacy

Stagefold does not control presentation slides, connect to remote devices, or require an account. It does not collect analytics, display ads, or offer purchases. See the [privacy policy](privacy.md).

For help, use the [support repository](https://github.com/valimikayilov/free-app-support). If you open a public issue, describe the problem and macOS version without posting private agenda notes, speaker details, or personal files.
