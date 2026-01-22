# CompressJpeg Function

## Syntax

[C#] void CompressJpeg(int quality) [Visual Basic] Sub CompressJpeg(quality As Integer)

may throw Exception()

## Params

## Notes

Compresses the image using JPEG compression.

JPEG compression can be used on RGB, Grayscale, CMYK or Separation images. It offers high compression levels for continuous tone images like photographs. However it is a lossy method which means that the quality of the compressed image will not be as good as the uncompressed image.

The quality of the compression can range from zero (lowest quality, highest compression) to 100 (highest quality, lowest compression). A good generic value is 75.

## Example

See the Recolor function.

Also see example code in: RecolorOperation Recolor Function.

