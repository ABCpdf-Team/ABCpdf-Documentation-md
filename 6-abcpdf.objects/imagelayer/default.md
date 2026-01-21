# ImageLayer Class

A generic bitmap layer appearing on a page of the document.

The actual bitmap data is held separately in a PixMap object. The ImageLayer merely references the bitmap and describes where and how it should be drawn. This is analogous to the way that images are embedded in HTML.

``` System.Object WebSupergoo.ABCpdf13.Objects.IndirectObject WebSupergoo.ABCpdf13.Objects.StreamObject WebSupergoo.ABCpdf13.Objects.Layer WebSupergoo.ABCpdf13.Objects.ImageLayer ```

## Method Description &nbsp; inherited methods... &nbsp;

## Property Description ImageName The name used to identify the PixMap in the Page resources. PixMap The PixMap containing the image data. &nbsp; inherited properties...