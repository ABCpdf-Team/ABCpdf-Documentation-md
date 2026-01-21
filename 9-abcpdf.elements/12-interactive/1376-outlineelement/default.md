---
title: "default"
css: "abcpdf-docs.css"
---

# OutlineElement Class

This class represents the outline dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 152, page 368.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=376)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 150, page 442.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because CatalogElement.EntryOutlines and OutlineItemElement.EntryParent require it to be so.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.OutlineElement ```

## Method Description OutlineElement Create a new OutlineElement. inherited methods... &nbsp;

## Property Description EntryType Represents the "Type" entry of the outline dictionary object. EntryFirst Represents the "First" entry of the outline dictionary object. EntryLast Represents the "Last" entry of the outline dictionary object. EntryCount Represents the "Count" entry of the outline dictionary object. inherited properties...