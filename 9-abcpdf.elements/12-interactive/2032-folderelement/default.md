# FolderElement Class

This class represents the folder dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 159, page 450.](https://www.iso.org/standard/63534.md)

[Adobe Supplement to the ISO 32000, BaseVersion: 1.7, ExtensionLevel: 3; Table: 8.6c, page 32.](http://www.adobe.com/content/dam/Adobe/en/devnet/acrobat/pdfs/adobe_supplement_iso32000.pdf#page=32)

This class is always an indirect object because CollectionElement.EntryFolders, FolderElement.EntryChild, FolderElement.EntryNext and FolderElement.EntryParent require it to be so.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.FolderElement ```

## Method Description FolderElement Create a new FolderElement. inherited methods... &nbsp;

## Property Description EntryType Represents the "Type" entry of the folder dictionary object. EntryID Represents the "ID" entry of the folder dictionary object. EntryName Represents the "Name" entry of the folder dictionary object. EntryParent Represents the "Parent" entry of the folder dictionary object. EntryChild Represents the "Child" entry of the folder dictionary object. EntryNext Represents the "Next" entry of the folder dictionary object. EntryCI Represents the "CI" entry of the folder dictionary object. EntryDesc Represents the "Desc" entry of the folder dictionary object. EntryCreationDate Represents the "CreationDate" entry of the folder dictionary object. EntryModDate Represents the "ModDate" entry of the folder dictionary object. EntryThumb Represents the "Thumb" entry of the folder dictionary object. EntryFree Represents the "Free" entry of the folder dictionary object. inherited properties...