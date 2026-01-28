# Decompress Function

## Syntax

[C#] bool Decompress()

## Params

## Notes

This method removes all compression from the stream.

Under some circumstances it may not be possible to fully decompress the stream. In these situations the function will return false.

In occasional and unusual situations, decompression may change the document to a greater extent than one might expect. For example if a PixMap is JPEG 2000 compressed it may contain interleaved transparency. Because interleaved transparency is only permitted in JPEG 2000 images, at the point of decompression the alpha needs to be separated off into a separate PixMap.SMask entry. However this type of situation is uncommon and normally the effects of decompression are limited to the object being decompressed.

## Example

None.

