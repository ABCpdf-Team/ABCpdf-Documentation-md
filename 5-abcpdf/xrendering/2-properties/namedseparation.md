# NamedSeparation Property

## Notes

Named separations to be used in addition to the color channels specified in the ColorSpace.

Separate color channels for the named separations are only created if the output type is TIFF and the output color space is CMYK or RGB.

If these conditions are met, ABCpdf will write each separation to a different TIFF page and set the TIFF ink name to the name of that separation.

This property can be either a comma separated list of the named separations, or it can be the keyword 'All' which indicates that all named separations referenced by the page should be output. You can obtain the ink names using the Page.GetNamedSeparations function.

For example, the following code will create a tiff file with 5 separated colors, each written to its own page. The ink name for each page will be the name of the separation plane: 'Cyan', 'Magenta', 'Yellow', 'Black' and 'Fluorescent Orange'.

[C#] doc.Rendering.NamedSeparation ="Fluorescent Orange"; doc.Rendering.ColorSpace = XRendering.ColorSpaceType.Cmyk; doc.Rendering.Save("separated.tiff");

Note that ABCpdf will not create spot colors if it encounters a page group color space that is different from the specified color space. However in this situation it will still write the process colors individually to the TIFF output.

## Example

None.

