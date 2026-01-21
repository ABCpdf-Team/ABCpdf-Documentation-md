---
title: "default"
css: "abcpdf-docs.css"
---

# CMapStreamElement Class

This class represents the cmap stream dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 120, page 277.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=285)

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 118, page 336.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because it is also a StreamElement and these are always indirect objects.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.CMapStreamElement ```

## Method Description CMapStreamElement Create a new CMapStreamElement. inherited methods... &nbsp;

## Property Description StreamElement The StreamElement associated with this class. EntryType Represents the "Type" entry of the cmap stream dictionary object. EntryCMapName Represents the "CMapName" entry of the cmap stream dictionary object. EntryCIDSystemInfo Represents the "CIDSystemInfo" entry of the cmap stream dictionary object. EntryWMode Represents the "WMode" entry of the cmap stream dictionary object. EntryUseCMap Represents the "UseCMap" entry of the cmap stream dictionary object. inherited properties...