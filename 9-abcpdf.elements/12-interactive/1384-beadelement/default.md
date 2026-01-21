# BeadElement Class

This class represents the bead dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 161, page 376.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=384)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 163, page 457.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because BeadElement.EntryN, BeadElement.EntryV, PageObjectElement.EntryB, ThreadActionElement.EntryB and ThreadElement.EntryF require it to be so.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.BeadElement ```

## Method Description BeadElement Create a new BeadElement. inherited methods... &nbsp;

## Property Description EntryType Represents the "Type" entry of the bead dictionary object. EntryT Represents the "T" entry of the bead dictionary object. EntryN Represents the "N" entry of the bead dictionary object. EntryV Represents the "V" entry of the bead dictionary object. EntryP Represents the "P" entry of the bead dictionary object. EntryR Represents the "R" entry of the bead dictionary object. inherited properties...