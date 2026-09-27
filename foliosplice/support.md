# FolioSplice support

FolioSplice is a free native macOS 14+ PDF page organizer. It is currently in preparation for App Store review; this page does not indicate public availability.

## Arrange a document

Add one or more PDFs, or choose **Try sample pages** in the empty workspace. Click a page to select it. Command-click toggles pages; Shift-click extends selection. The range field accepts `1, 3-5`, `all`, `odd`, or `even`, using the current page order.

Move selections earlier/later, rotate, duplicate, or remove them. Drag one page onto another to place it before that page. Undo/redo retains the latest 30 edits. The right-hand preview displays the focused page; source filename and page number stay visible.

## Export and split

**Export PDF** writes the entire arrangement. **Export selected pages** keeps selected pages in their current order. **Split into new folder** writes consecutive groups of the specified size into a newly created folder. Existing files are never overwritten; choose a new filename if one already exists. **Show export** reveals the result in Finder.

The workspace is kept in memory and does not restore after quitting. Export a PDF before quitting to keep your arrangement. Your original PDF files remain unchanged. New workspace releases loaded source PDFs.

## Scope and limits

FolioSplice assembles PDF pages. It does not edit text, perform OCR, compress PDFs, or redact content. Export may not preserve document-level bookmarks, interactive forms, digital signatures, or accessibility tags. Review the exported PDF before sharing. For preservation-critical documents, keep the original file.

Encrypted and assembly-restricted PDFs are unsupported. Use the source application to export an unlocked, editable copy first. Each PDF may be at most 40 MB. A workspace holds up to 100 MB of loaded sources and 1,000 arranged pages. Removed pages' sources remain loaded to support Undo until you start a new workspace. These are stability limits, not paid tiers.

## Privacy and help

The app processes PDFs locally and has no account, ads, analytics, purchases, or network entitlement. See [the privacy policy](privacy.md).

For help, [open a support issue](https://github.com/valimikayilov/free-app-support/issues). Include the macOS/app version, the operation, and the exact error. Do not post private PDFs, passwords, or confidential details. If an example is needed, create a non-sensitive sample that reproduces the issue.
