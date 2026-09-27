# ChromaMoor support

ChromaMoor is a free, offline palette and text-contrast utility for macOS 14 or later. No account, advertisements, purchases, or subscription.

## Build a palette

Choose a palette from the sidebar, or create a new one. Each palette can contain 1–16 swatches, and the library supports up to 40 palettes. Use Palette options to rename, duplicate, or remove the selected palette. At least one palette and one swatch must remain.

Click a swatch to edit its name and HEX value or use the macOS color picker. HEX accepts three or six digits, with an optional `#`. Colors are opaque, 8-bit sRGB; alpha values and named colors are not supported. Swatch menus offer HEX/RGB/HSL copying, earlier/later reordering, removal, and contrast-pair selection.

Palette names allow 1–60 characters and swatch names 1–40. Undo and Redo retain up to 30 palette changes during the current session. They do not provide permanent version history.

## Check text contrast

Use a swatch as the text color or background, or enter HEX values in the contrast panel. Valid pairs update the preview and save locally. An invalid HEX field shows an explanation and keeps the last valid pair. Swap exchanges text and background.

The app checks WCAG 2.2 text-color contrast thresholds: AA requires 4.5:1 for normal text and 3:1 for large text; AAA requires 7:1 and 4.5:1 respectively. Large text means at least 18 pt, or 14 pt bold. The shown ratio is rounded, but pass/fail uses the unrounded value. A displayed 4.50 can therefore fail a 4.5 threshold when the actual result is slightly lower.

This is a color-contrast check, not a complete accessibility audit. Font rendering, text size, background imagery, and other accessibility requirements need separate review.

## Extract from an image

Switch to From image and choose a local image, or try the included original Coastal Study artwork. Request 2, 4, 6, 8, 12, or 16 colors. Similar colors are grouped, so fewer colors may be returned. Add as new palette saves the resulting colors for editing.

Supported ImageIO-readable formats are PNG, JPEG, HEIC, TIFF, BMP, GIF, and WebP, with a 100 MB file limit and 40-megapixel image limit. ChromaMoor reads the first frame, applies orientation, downsamples to fit 256 × 256 pixels, converts to sRGB, and places transparent pixels over white. Percentages refer to the sampled groups and may not sum to exactly 100 because of rounding. The source file is never changed. Images are held in memory during the session and are not saved in the palette library. Cancellation is checked between processing stages; an active system decoder may finish before cancellation takes effect.

## Export and transfer

Export the selected palette as ChromaMoor JSON, CSS custom properties, or an SVG swatch sheet. CSS variable names are sanitized and numbered to remain distinct. SVGs use solid swatches and text; long display names are shortened visually, with complete names retained in SVG titles. Copy CSS puts the selected palette's CSS on the clipboard.

Export library backup saves every palette and the last valid contrast pair as JSON. Import palette or library validates a ChromaMoor version 1 file and adds new palette copies with new identifiers. It keeps the current contrast pair. Importing a library must keep the total at 40 palettes or fewer. Palette files are limited to 100 KB; libraries to 1 MB. Other apps' JSON formats are not supported.

Exports require a new filename. Existing files or symbolic links are never overwritten. You control where to save and whether to share exports.

## Local saving and recovery

The library and last valid contrast pair are automatically saved inside the app's local Application Support folder in its macOS sandbox. Show local storage opens the saved file's location. There is no account or cloud sync.

If saving fails, a visible warning offers Retry save and Export library backup. Closing or quitting warns about unsaved changes. If the saved library cannot be read, the original file is preserved. Back up & reset first copies the unreadable file to a uniquely named backup and then creates a fresh library. Export the current session before resetting if you want to keep it. Backups remain local until you manage them yourself.

## Help

Open a [public support issue](https://github.com/valimikayilov/free-app-support/issues), with your macOS version and the steps involved. Do not include confidential images, palettes, or personal information.

[Privacy policy](privacy.md)
