# RasterNest support

RasterNest prepares batches of still images on your Mac. All features are free. The first release is in preparation.

## Prepare a batch

Choose **Add images**, use the folder button, or drop image files/folders into the window. Folder import adds supported images directly inside that folder; it does not scan subfolders. Each batch supports up to 1,000 images.

Supported inputs include JPEG, PNG, HEIC, TIFF, BMP, WebP, and still GIF, using macOS image decoders. Animated and multi-page files are rejected. Some specialized or damaged files may not decode.

The built-in sample images are original geometric illustrations and can be used to try every export setting.

## Choose output settings

Choose JPEG, PNG, or HEIC. Set original dimensions, a longest edge, or a bounding box. Proportions are preserved without cropping or stretching. Enlargement is off by default. Output is limited to 12,000 pixels per side and 64 megapixels.

PNG retains transparency. JPEG and HEIC use a white background for transparent pixels. Exports use 8-bit sRGB color, so this is not a workflow for retaining HDR or high-bit-depth master images.

Select an image to see its original or encoded preview. The output dimensions and encoded size apply to that image, not the whole batch. Other images can have different output sizes.

Use original filenames or a prefix with a three-digit minimum counter. Duplicate output names receive a suffix. Save a named recipe to reuse settings on this Mac.

## Export safely

Choose **Export batch** and select a destination. RasterNest creates a new folder for each run. It does not replace original images or existing exports. Keep originals until you have checked the results.

**Stop** finishes the current image and leaves completed exports in place. Each successful file is marked Exported. Select a failed file to see its error. **Show export folder** reveals the results in Finder.

The batch list is not restored after quitting. Saved recipes and current settings remain on this Mac. If settings cannot be read, the file is preserved and the app uses defaults for that session.

## Metadata and privacy

Source photo tags, including EXIF and GPS, are not copied into exports. Visible text, faces, addresses, and other information inside the picture remain visible. Filenames can also contain personal information. Read the [privacy policy](privacy.md).

## Get help

[Open a support issue](https://github.com/valimikayilov/free-app-support/issues/new) with the macOS version, app version, output settings, file format, and steps to reproduce the problem. GitHub requires an account, and issues are public. Do not include private images, private paths, personal information, or confidential metadata.
