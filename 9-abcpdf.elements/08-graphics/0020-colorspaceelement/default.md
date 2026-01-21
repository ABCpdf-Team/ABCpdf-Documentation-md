# ColorSpaceElement Class

This class represents a color space.

Sub-classes represent different types of color spaces.

Internally within a PDF document color spaces are represented as an array of values with the first element being the type of color space.

However as a shorthand, if there is only one element in the array, the name can be used without an enclosing array.

This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 62, page 139.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=147)

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ColorSpaceElement WebSupergoo.ABCpdf13.Elements.CalGrayColorSpaceElement WebSupergoo.ABCpdf13.Elements.CalRGBColorSpaceElement WebSupergoo.ABCpdf13.Elements.DeviceColorSpaceElement WebSupergoo.ABCpdf13.Elements.DeviceNColorSpaceElement WebSupergoo.ABCpdf13.Elements.ICCBasedColorSpaceElement WebSupergoo.ABCpdf13.Elements.IndexedColorSpaceElement WebSupergoo.ABCpdf13.Elements.LabColorSpaceElement WebSupergoo.ABCpdf13.Elements.PatternColorSpaceElement WebSupergoo.ABCpdf13.Elements.SeparationColorSpaceElement ```

## Method Description ColorSpaceElement Create a new ColorSpaceElement. inherited methods... &nbsp;

## Property Description ColorSpace This property represents the type of color space. inherited properties...