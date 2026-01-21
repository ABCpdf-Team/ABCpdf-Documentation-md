# CIDFontElement Class

This class represents the cidfont dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 117, page 269.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=277)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 115, page 327.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because it inherits from FontElement which is always an indirect object.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.FontElement WebSupergoo.ABCpdf13.Elements.CIDFontElement ```

## Method Description CIDFontElement Create a new CIDFontElement. inherited methods... &nbsp;

## Property Description EntrySubtype Represents the "Subtype" entry of the cidfont dictionary object. EntryBaseFont Represents the "BaseFont" entry of the cidfont dictionary object. EntryCIDSystemInfo Represents the "CIDSystemInfo" entry of the cidfont dictionary object. EntryFontDescriptor Represents the "FontDescriptor" entry of the cidfont dictionary object. EntryDW Represents the "DW" entry of the cidfont dictionary object. EntryW Represents the "W" entry of the cidfont dictionary object. EntryDW2 Represents the "DW2" entry of the cidfont dictionary object. EntryW2 Represents the "W2" entry of the cidfont dictionary object. EntryCIDToGIDMap Represents the "CIDToGIDMap" entry of the cidfont dictionary object. inherited properties...