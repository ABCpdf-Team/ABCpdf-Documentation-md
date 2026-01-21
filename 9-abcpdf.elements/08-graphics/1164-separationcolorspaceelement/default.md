---
title: "default"
css: "abcpdf-docs.css"
---

# SeparationColorSpaceElement Class

This class represents a separation color space.

A separation color space represents a single custom color. Most typically these are spot colors used in printing.

For example the conventional color space for printing is CMYK and for that you can use the DeviceCMYK color space.

However you might wish to add support for a custom ink like gold or silver which will print correctly when passed to a printer which supports this ink.

The separation color space includes a conversion function so that it will also provide a good representation on screen and on normal CMYK printers.

This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Section: 8.6.6.4, page 157.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=165)

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ColorSpaceElement WebSupergoo.ABCpdf13.Elements.SeparationColorSpaceElement ```

## Method Description SeparationColorSpaceElement Create a new SeparationColorSpaceElement. inherited methods... &nbsp;

## Property Description EntryName This property represents the name of the separation color space. EntryAlternateColorSpace This property represents the alternate color space for this Separation color space. EntryTintTransform This property represents the tint transform function. inherited properties...