# Gray Property

## Notes

Allows you to get or set the gray level.

Grayscale levels can range from 0 (black) to 255 (white).

Querying this property does not change the ColorSpace. This means you can obtain approximate Grayscale values for RGB or CMYK colors.

However if you change the value of this property the color will automatically be converted to Grayscale.

This property can also be used to specify levels for spot colorants. Levels can range from 0 (0% intensity) to 255 (100% intensity). See the AddColorSpaceSpot method for an example.

## Example

Also see example code in: Doc AddColorSpaceSpot Function, SwfImportOperation Import Function.

