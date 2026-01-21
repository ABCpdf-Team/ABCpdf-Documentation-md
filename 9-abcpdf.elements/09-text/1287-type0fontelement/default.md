---
title: "default"
css: "abcpdf-docs.css"
---

# Type0FontElement Class

This class represents the type 0 font dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 121, page 279.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=287)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 119, page 338.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because it inherits from FontElement which is always an indirect object.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.FontElement WebSupergoo.ABCpdf13.Elements.Type0FontElement ```

## Method Description Type0FontElement Create a new Type0FontElement. inherited methods... &nbsp;

## Property Description EntrySubtype Represents the "Subtype" entry of the type 0 font dictionary object. EntryBaseFont Represents the "BaseFont" entry of the type 0 font dictionary object. EntryEncoding Represents the "Encoding" entry of the type 0 font dictionary object. EntryDescendantFonts Represents the "DescendantFonts" entry of the type 0 font dictionary object. EntryToUnicode Represents the "ToUnicode" entry of the type 0 font dictionary object. inherited properties...