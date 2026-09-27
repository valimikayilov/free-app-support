# LineHarbor help

LineHarbor is a free native macOS 14+ app for comparing two plain texts locally. It has no accounts, subscriptions, in-app purchases, advertisements, or analytics. Release status: in preparation for App Store review.

## Compare two texts

1. Type into Original and Revision, use their Paste buttons, or choose Open UTF-8 to import a text file. Importing copies the text into memory; original files are never modified.
2. Give each side a title if useful. Swap exchanges both titles and texts.
3. Choose Keep whitespace, Trim line edges, or Collapse spaces & tabs. The latter two affect ordinary spaces and tabs, not all Unicode whitespace. Ignore case uses Unicode lowercasing with a fixed locale.
4. Choose Compare Texts or press Command-Return. Review shows line numbers, added/removed/changed rows, and differences ignored by your options. A changed row pairs consecutive removals/additions; this is a review tool, not an automatic merge or patch generator.
5. Turn on Only differences to hide unchanged rows. Use the arrows, or Option-Command-J/K, to move between differences. Ignored rows remain visible and navigable.

CRLF and CR line endings are always normalized to LF for comparison. A final empty row represents a final newline. Comparison preserves the distinction between different UTF-8 sequences in the default mode, including canonically equivalent Unicode text. The middle span of changed lines is emphasized between their common prefix and suffix; it is not a word-by-word diff.

Try sample loads two original workshop plans. Replacing a nonempty workspace or text pane prompts first where appropriate. Standard editor undo and text selection/copy are available. Editing text, titles, or comparison options invalidates the previous result; compare again before exporting a report.

## Save and reopen

Save Draft writes a new `.lineharbor.json` file containing both full texts, titles, and options. Open Draft reloads this format and compares it. Drafts are not autosaved. Quit and window close warn about unsaved content. Opening the app after quitting starts a new workspace.

Export HTML writes a standalone, printable side-by-side report with every row, even when Only differences is selected. It contains both complete texts and uses no scripts, fonts, or remote resources. It is not an editable draft. You can open the report in your browser and print it using the browser's normal print controls.

Both export formats may contain private text you supplied. Keep them private or share them deliberately. Existing export destinations are never overwritten; use a new filename.

## Limits and troubleshooting

- UTF-8 plain-text input only. An optional UTF-8 byte-order mark is accepted and removed when importing a file. Word, PDF, RTF, UTF-16, folders, and symbolic links are unsupported.
- Up to 500,000 UTF-8 bytes and 3,000 lines per side, including the final newline marker; up to 10,000 UTF-16 code units per line. Null bytes are rejected. Split larger input before comparing.
- Comparison runs in the background and can be cancelled. Both input texts remain available after cancellation.
- Drafts use LineHarbor format version 1 and must be no larger than 6.5 MB. Other JSON formats are not supported.
- A red or orange change means the texts differ under the selected options; it does not judge whether either version is correct.

## Contact

[Ask for help or report a problem](https://github.com/valimikayilov/free-app-support/issues/new). Issues are public; describe the issue without sharing personal or confidential text.
