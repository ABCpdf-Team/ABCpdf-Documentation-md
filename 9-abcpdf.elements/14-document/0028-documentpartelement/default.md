---
title: "default"
css: "abcpdf-docs.css"
---

# DocumentPartElement Class

This class represents the dpart dictionary. This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-2:2017 PDF 2.0; Table: 409, page 829.](https://www.iso.org/standard/63534.md)

This class is always an indirect object because DocumentPartGoToActionElement.EntryDp, DpartElement.EntryDParts, DpartElement.EntryParent, DpartrootElement.EntryDPartRootNode and PageObjectElement.EntryDPart require it to be so.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.DocumentPartElement ```

## Method Description DocumentPartElement Create a new DocumentPartElement. inherited methods... &nbsp;

## Property Description EntryType Represents the "Type" entry of the dpart dictionary object. EntryParent Represents the "Parent" entry of the dpart dictionary object. EntryDParts Represents the "DParts" entry of the dpart dictionary object. EntryStart Represents the "Start" entry of the dpart dictionary object. EntryEnd Represents the "End" entry of the dpart dictionary object. EntryDPM Represents the "DPM" entry of the dpart dictionary object. EntryAF Represents the "AF" entry of the dpart dictionary object. inherited properties...