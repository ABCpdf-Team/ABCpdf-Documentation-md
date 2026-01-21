# DocumentInformationElement Class

This class represents the document information dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 317, page 550.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=558)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 349, page 712.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because CrossReferenceStreamElement.EntryInfo and FileTrailerElement.EntryInfo require it to be so.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.DocumentInformationElement ```

## Method Description DocumentInformationElement Create a new DocumentInformationElement. inherited methods... &nbsp;

## Property Description EntryTitle Represents the "Title" entry of the document information dictionary object. EntryAuthor Represents the "Author" entry of the document information dictionary object. EntrySubject Represents the "Subject" entry of the document information dictionary object. EntryKeywords Represents the "Keywords" entry of the document information dictionary object. EntryCreator Represents the "Creator" entry of the document information dictionary object. EntryProducer Represents the "Producer" entry of the document information dictionary object. EntryCreationDate Represents the "CreationDate" entry of the document information dictionary object. EntryModDate Represents the "ModDate" entry of the document information dictionary object. EntryTrapped Represents the "Trapped" entry of the document information dictionary object. inherited properties...