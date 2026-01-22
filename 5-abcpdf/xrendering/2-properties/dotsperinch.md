# DotsPerInch Property

## Notes

This property determines the resolution of the output image.

Because PDF documents specify distances in physical units (typically points) a resolution unit is needed to convert these physical units to pixel based units.

For example a document 612 points wide rendered at 144 DPI will result in an output image 1224 pixels wide.

Changing this property will change the values of both the DotsPerInchX and DotsPerInchY properties.

## Example

See the DefaultHalftone property.

Also see example code in: ABCpdf PDF Rendering Example, XRendering AntiAliasPolygons Property, XRendering AntiAliasText Property, XRendering ColorSpace Property, XRendering DefaultHalftone Property, XRendering IccCmyk Property, XRendering Overprint Property, XRendering SaveQuality Property, Page GetBitmap Function, Page Thumbnail Property, PixMap GetBitmap Function, RenderOperation Save Function.

