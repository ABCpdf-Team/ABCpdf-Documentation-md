# CompressCcitt Function

## Syntax

[C#] void CompressCcitt()

may throw Exception()

## Params

## Notes

Compresses the image using CCITT compression.

CCITT compression can only be used on black and white images. It is optimized for the lossless compression of scanned documents and faxes.

If the values of both the BitsPerComponent and the Components is one then the PixMap can be compressed using this method. If not then calling this method will generate an exception.

## Example

None.

