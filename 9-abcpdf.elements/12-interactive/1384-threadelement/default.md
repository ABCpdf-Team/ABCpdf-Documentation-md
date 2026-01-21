---
title: "default"
css: "abcpdf-docs.css"
---

# ThreadElement Class

This class represents the thread dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 160, page 376.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=384)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 162, page 457.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because BeadElement.EntryT, CatalogElement.EntryThreads and ThreadActionElement.EntryD require it to be so.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ThreadElement ```

## Method Description ThreadElement Create a new ThreadElement. inherited methods... &nbsp;

## Property Description EntryType Represents the "Type" entry of the thread dictionary object. EntryF Represents the "F" entry of the thread dictionary object. EntryI Represents the "I" entry of the thread dictionary object. inherited properties...