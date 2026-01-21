---
title: "default"
css: "abcpdf-docs.css"
---

# PageTreeNodeElement Class

This class represents the page tree node. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 29, page 76.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=84)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 30, page 102.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because CatalogElement.EntryPages, PageObjectElement.EntryParent, PageTreeNodeElement.EntryKids and PageTreeNodeElement.EntryParent require it to be so.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.PageTreeNodeElement ```

## Method Description PageTreeNodeElement Create a new PageTreeNodeElement. inherited methods... &nbsp;

## Property Description EntryType Represents the "Type" entry of the page tree node object. EntryParent Represents the "Parent" entry of the page tree node object. EntryKids Represents the "Kids" entry of the page tree node object. EntryCount Represents the "Count" entry of the page tree node object. EntryResources Represents the "Resources" entry of the page tree node object. EntryMediaBox Represents the "MediaBox" entry of the page tree node object. EntryCropBox Represents the "CropBox" entry of the page tree node object. EntryRotate Represents the "Rotate" entry of the page tree node object. inherited properties...