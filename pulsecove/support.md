# PulseCove help

PulseCove is a free, offline click-track builder for macOS 14 or later. Create practice rhythms with bar-by-bar tempo ramps, accents, subdivisions, and silence; preview the result and export a WAV file. No account, advertising, subscriptions, or purchases.

## Make a track

1. Start with the current project or choose a starting point in the sidebar. A preset replaces the current project; Undo restores it during the session.
2. Add sections, select one, and choose **Edit section**. Set its name, bars, beats per bar, start/end BPM, subdivisions, and accents. Use the arrows to reorder sections, or duplicate a section.
3. Set the count-in, click voice, and output level. **Render track** builds the waveform and audio. Editing stops playback and clears the previous render.
4. Play, pause, stop, or seek through the track. Loop repeats the entire track, including the count-in. Loop is a preview setting and does not repeat the exported file.
5. **Export WAV** saves 44.1 kHz, mono, 16-bit PCM audio. Choose a new filename; existing files are preserved.

## Timing rules

BPM counts the numbered beats; there is no time-signature denominator. For a section with several bars, the tempo moves evenly from the start BPM in the first bar to the end BPM in the final bar. It changes at each bar boundary, not continuously within a bar. One-bar sections use only the start BPM.

Choose 1, 2, 3, or 4 clicks per beat. Swing only applies to two-part subdivisions: 50% is straight; 75% places the second click three-quarters of the way through the beat. Subdivision clicks are quieter. A Strong accent is louder and higher in pitch than Normal. Rest mutes every click in that beat, including subdivisions.

A count-in uses the first section's beat count and starting tempo, with one click per beat and a strong first beat. It ignores that section's subdivisions and rests. Audio is rendered to a fixed sample timeline before playback. Playback position and beat readouts are visual guides, not external device synchronization. PulseCove does not provide MIDI clock, recording, background agents, or DAW integration.

## Projects and recovery

One current project saves automatically in the app's local sandbox. Export project JSON to keep multiple projects. Import previews the title, sections, bars, and duration. Confirming import first saves a separate recovery copy of the current project. Import never modifies its source file.

Undo and Redo retain the last 20 project changes for the current app session; they stop playback and clear the render. Use the sidebar buttons or Option-Command-Z and Option-Shift-Command-Z. Normal Command-Z remains available to the text editor.

If saving fails, the app shows Retry Save and Export Project. Closing or quitting warns about unsaved changes. An unreadable saved project is preserved; Back Up and Reset keeps a separate copy before creating a default project. Export any new unsaved edits first. Show Saved File reveals the storage folder and recovery copies.

Limits: 20 sections; 1–128 bars and 1–12 beats per section; 20–300 BPM; 10 minutes including count-in; 100 KB JSON projects. Project titles allow 60 characters and section names 40, with additional UTF-8 byte limits. The level control affects both preview and WAV output. If you cannot hear playback, check your Mac's chosen audio output and volume.

## Support

[Report a problem or ask for help](https://github.com/valimikayilov/free-app-support/issues/new). Issues are public. Describe the steps, macOS version, and expected result without sharing private project files or personal information.
