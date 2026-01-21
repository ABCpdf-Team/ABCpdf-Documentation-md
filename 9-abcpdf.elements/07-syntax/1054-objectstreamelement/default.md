# ObjectStreamElement Class

This class represents the object stream dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 16, page 46.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=54)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 16, page 61.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because it is also a StreamElement and these are always indirect objects.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ObjectStreamElement ```

## Method Description ObjectStreamElement Create a new ObjectStreamElement. inherited methods... &nbsp;

## Property Description StreamElement The StreamElement associated with this class. EntryType Represents the "Type" entry of the object stream dictionary object. EntryN Represents the "N" entry of the object stream dictionary object. EntryFirst Represents the "First" entry of the object stream dictionary object. EntryExtends Represents the "Extends" entry of the object stream dictionary object. inherited properties...