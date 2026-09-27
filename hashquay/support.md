# HashQuay support

HashQuay is a free native macOS 14+ file-checksum utility. It is in preparation for App Store review; this page does not indicate public availability.

## Calculate and compare

Choose **Add files**, drop regular files into the workspace, or try the included sample files. HashQuay reads each file in blocks and calculates SHA-256, SHA-512, SHA-1, and MD5 in one pass. Select a row to inspect or copy a checksum. Paste an expected hexadecimal value to see whether it matches. Outer whitespace and uppercase letters are accepted when comparing a pasted checksum.

The workspace supports up to 500 files. Folders and symbolic links are not imported. Files are processed sequentially; Cancel stops after the current block and retains previously completed results. Recalculate all checks the current contents again. Keep source files unchanged during calculation. The file size is checked, but simultaneous edits with the same size are not reliably detected.

A checksum describes file contents. It does not establish who published the file, scan for malware, or prove a source is trustworthy. Compare against an expected checksum from a source you trust. SHA-1 and MD5 are included for legacy compatibility; use SHA-256 or SHA-512 for security-sensitive comparisons. Matching SHA-256 values are highlighted when several workspace files share one.

## Export and verify

**Export CSV report** records filenames, byte counts, and all four hashes for calculated files. **Export manifest** creates a HashQuay JSON manifest with the same data. Existing files are never overwritten: choose a new filename. Failed or cancelled files are excluded from exports. Full source paths are not included.

**Verify manifest** opens a HashQuay version 1 JSON manifest, then asks for the folder containing its files. This replaces the workspace. Files are matched by their exact names directly inside that folder; subfolders are not searched. Each row reports Verified, Mismatch, or Could not read. Verification compares the file size and all four hashes. Manifests need unique filenames, including case/accent-insensitive comparisons, and cannot contain path separators or control characters. Only HashQuay manifests are supported; this is not a general parser for third-party `.sha256` files.

Results and selected file references stay in memory. Export before closing the app to keep results. Original files remain unchanged. Reopening the app starts a new workspace. Sample files are original demonstration content stored in the app's temporary directory.

## Privacy and help

There are no accounts, purchases, ads, analytics, third-party SDKs, or network entitlement. All file processing is local. See [the privacy policy](privacy.md).

For help, [open a support issue](https://github.com/valimikayilov/free-app-support/issues). Include the app/macOS version, the operation, and the error message. Issues are public; do not attach private files, checksums of sensitive content, or confidential filenames. Use a non-sensitive test file to demonstrate an issue.
