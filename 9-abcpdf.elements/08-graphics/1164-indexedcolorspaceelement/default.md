# IndexedColorSpaceElement Class

This class represents an indexed color space.

Indexed color spaces represent a set of colors from a palette. Each color is identified using an index into the palette.

The palette itself needs to be defined in terms of another color space such as DeviceRGB or DeviceCMYK. So in many ways an indexed color space is a meta color space.

This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Section: 8.6.6.3, page 156.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=164)

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ColorSpaceElement WebSupergoo.ABCpdf13.Elements.IndexedColorSpaceElement ```

## Method Description IndexedColorSpaceElement Create a new IndexedColorSpaceElement. inherited methods... &nbsp;

## Property Description EntryBaseColorSpace This property represents the underlying color space for this Indexed color space. EntryHiVal This property represents the highest number used to index into the palette. EntryLookup This property represents the lookup table for the palette. inherited properties...