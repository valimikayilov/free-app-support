# RecallPier support

RecallPier is a free, offline study-card workspace for macOS 14 or later. Create your own decks, recall an answer before revealing it, and choose an honest rating. It has no account, advertising, purchases, analytics, cloud sync, or AI service.

## Start studying

The included Everyday math deck contains eight original example cards. Choose **Review due cards** for scheduled study, or **Practice cards** to revisit active cards without changing their due times. Session limits are 20, 50, or 100 cards. Paused cards are excluded from both modes.

Scheduled queues put previously reviewed due cards before new cards. Practice queues include future-due cards too, ordered by existing due time before new cards. The queue is fixed when the session starts. Each card appears once per session; a card rated Again can be reviewed in another session after 10 minutes. Leaving a session keeps completed ratings but discards its remaining queue.

An optional scratch answer helps you recall before revealing the answer. It is not automatically marked, saved, or exported. Compare it yourself. Scratch answers are cleared after each card or when the session ends.

## The schedule is visible

All new cards start at step 0. Scheduled ratings behave as follows:

- **Again:** due in 10 minutes; reset to step 0.
- **Hard:** due in 1 day; keep the current step.
- **Good:** use the interval for the current step, then advance one step.
- **Easy:** use the next step's interval, then advance two steps.

The intervals for steps 0–6 are 1, 3, 7, 14, 30, 60, and 120 days. Step 7 is the maximum and also uses 120 days. Easy never exceeds 120 days. A day means 24 elapsed hours; local displayed times may shift when daylight saving changes. RecallPier uses this simple fixed schedule, not a prediction of memory or a guarantee of learning.

Practice ratings appear in recent history but leave scheduled steps, review counts, and due times unchanged. Ratings Today includes both modes in your current local calendar day, using retained history. The library retains the latest 5,000 ratings; the history window displays the latest 100. Removing cards/decks or resetting progress also removes their history.

## Build a library

Use **New deck** and **Add card**. Deck options support rename/description, duplication with fresh progress, portable export, progress reset, and removal. A copied or imported portable deck starts with fresh progress and no paused cards. Editing existing card text keeps its schedule. Pause excludes a card from both study modes until resumed.

Search questions, answers, and notes. Filters show All, Due, New, or Paused cards. Library Undo/Redo retains 20 changes or ratings during the current app session. Undo ends any active review session. Use the sidebar buttons or Option-Command-Z / Option-Shift-Command-Z. Ordinary Command-Z remains available to the native text editor.

Limits: 40 decks, 1,000 cards per deck, 5,000 cards overall; 60-character deck names, 300-character descriptions, 2,000-character questions, 4,000-character answers, and 2,000-character notes. Text also has UTF-8 byte limits to prevent oversized combining-character sequences. Unsupported control characters are rejected. Empty decks are allowed; questions and answers must contain text.

## Import and share

**Import or restore…** accepts UTF-8 CSV and RecallPier version 1 JSON. An import preview appears before the library changes.

CSV requires the exact columns `front,back` or `front,back,note` (header case and surrounding header whitespace are ignored). Fields containing commas, quotes, or line breaks must be quoted, with internal quotes doubled. UTF-8 BOM, LF, CR, and CRLF are accepted. Blank rows are ignored. At most 1,000 cards and 10 MB are accepted. Malformed rows reject the entire import. CSV is treated as text, never formulas or code. [Downloadable sample](sample.csv).

A portable deck JSON contains its name, description, questions, answers, and notes. It omits progress/history and paused status. Import adds it as a new deck with new identifiers. Portable files must be 10 MB or smaller.

**Export library backup…** includes all decks, selection, progress, paused status, and retained ratings. Libraries must be 20 MB or smaller. Restoring one replaces the current library after an explicit preview; RecallPier first saves a separate local recovery backup of the current library. Undo can also restore the previous state during that session. Files from other flashcard applications are not directly supported; use the documented CSV format.

Exports use the system save panel and require a new filename. Existing files and links are not overwritten. Import reads regular files only and does not alter source files. Keep backups somewhere you control; exporting to a cloud-synced folder lets that folder's provider handle the file.

## Storage and recovery

Changes and completed ratings save automatically in the app's local Application Support directory. There is no synchronization between computers. Session queues, scratch answers, filters, and Undo/Redo history are temporary.

A save failure shows a warning with retry, export, and Show Storage controls. Closing or quitting warns if changes remain unsaved. An unreadable saved library is preserved and saving is blocked until **Back Up and Reset** succeeds. That action keeps a recovery copy before creating a fresh example library. A library backup export can preserve your current in-memory work before resetting.

## Help

Open an issue in [the support repository](https://github.com/valimikayilov/free-app-support/issues) with your macOS version and steps to reproduce the problem. Avoid posting private card contents or personal information. Help and privacy links open your browser; no card data is sent to this repository by the app.
