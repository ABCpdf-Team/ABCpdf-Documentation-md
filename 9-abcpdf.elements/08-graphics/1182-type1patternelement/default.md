---
title: "default"
css: "abcpdf-docs.css"
---

# Type1PatternElement Class

This class represents the type 1 pattern dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 75, page 174.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=182)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 74, page 218.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because it is also a StreamElement and these are always indirect objects.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.PatternElement WebSupergoo.ABCpdf13.Elements.Type1PatternElement ```

## Method Description Type1PatternElement Create a new Type1PatternElement. inherited methods... &nbsp;

## Property Description StreamElement The StreamElement associated with this class. EntryPatternType Represents the "PatternType" entry of the type 1 pattern dictionary object. EntryPaintType Represents the "PaintType" entry of the type 1 pattern dictionary object. EntryTilingType Represents the "TilingType" entry of the type 1 pattern dictionary object. EntryBBox Represents the "BBox" entry of the type 1 pattern dictionary object. EntryXStep Represents the "XStep" entry of the type 1 pattern dictionary object. EntryYStep Represents the "YStep" entry of the type 1 pattern dictionary object. EntryResources Represents the "Resources" entry of the type 1 pattern dictionary object. EntryMatrix Represents the "Matrix" entry of the type 1 pattern dictionary object. inherited properties...