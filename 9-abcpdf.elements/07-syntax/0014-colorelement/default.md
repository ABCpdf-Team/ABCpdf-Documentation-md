# ColorElement Class

This class represents a color.

A color consists of an array of component values. For example an RGB color has three values between zero and one, a CMYK color has four between zero and one.

Colors only make sense in the context of a color space that specifies what the components represent. Most components range between zero and one.

However some color spaces such as Lab have components with values outside this range.

This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; page 139.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=147)

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ColorElement ```

## Method Description ColorElement Create a new ColorElement. GetColor Get the contents of this ColorElement as an XColor. SetColor Set the contents of this ColorElement using an XColor. inherited methods... &nbsp;

## Property Description Components The component intensities for the color. inherited properties...