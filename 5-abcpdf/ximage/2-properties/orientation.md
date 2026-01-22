# Orientation Property

## Notes

TIFF and JPEG files can contain an Orientation setting describing how the image would be most naturally viewed.

Postscript files can contain the DSC comment tag:%%Orientation: Landscape/Portraitthat describes how the image would be most naturally viewed. For Landscape orientation, this property becomes 90 degrees

For example an image may be rotated by 90 degrees or flipped horizontally. These kinds of settings are most commonly used when images are scanned and orientation is only determined at a later date, perhaps via OCR.

This property may take any of the following values:

By default the XImage will work with these settings to present the image the right way up. However you can select any presentation orientation by using the AppliedOrientation property to apply a transform of your choice.

## Example

None.

