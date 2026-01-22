# Components Property

## Notes

The number of color components for each pixel.

For example Grayscale images contain one component, RGB images contain three and CMYK images contain four.

Referencing this property has a number of advantages over referencing the PixMap.ColorSpace.Components property.

Firstly it avoids the possibility that a new ColorSpace object will need to be created.

Secondly it takes account of the fact that certain types of PixMap (e.g. ImageMasks) do not have a ColorSpace. In these cases the number of components is implicit in the definition of the PixMap and needs to be inferred by the PixMap itself.

## Example

None.

