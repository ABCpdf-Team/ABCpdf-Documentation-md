# Type1FontElement Class

This class represents the type 1 font dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 111, page 254.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=262)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 109, page 310.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because it inherits from FontElement which is always an indirect object.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.FontElement WebSupergoo.ABCpdf13.Elements.Type1FontElement ```

## Method Description Type1FontElement Create a new Type1FontElement. inherited methods... &nbsp;

## Property Description EntrySubtype Represents the "Subtype" entry of the type 1 font dictionary object. EntryName Represents the "Name" entry of the type 1 font dictionary object. EntryBaseFont Represents the "BaseFont" entry of the type 1 font dictionary object. EntryFirstChar Represents the "FirstChar" entry of the type 1 font dictionary object. EntryLastChar Represents the "LastChar" entry of the type 1 font dictionary object. EntryWidths Represents the "Widths" entry of the type 1 font dictionary object. EntryFontDescriptor Represents the "FontDescriptor" entry of the type 1 font dictionary object. EntryEncoding Represents the "Encoding" entry of the type 1 font dictionary object. EntryToUnicode Represents the "ToUnicode" entry of the type 1 font dictionary object. inherited properties...