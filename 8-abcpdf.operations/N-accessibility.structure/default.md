---
title: "default"
css: "abcpdf-docs.css"
---

# Structure Class

Represents the PDF tagged structure.

``` System.Object WebSupergoo.ABCpdf13.Operations.Structure ```

## Method Description Structure Create a new Structure based on the content in a doc. FindElementsByType Scan through the structure to find all structure elements of a particular type. GetPageNumber Get the page number for a particular page object. ExtractStructure Extract the structure in an HTML-like format that can be displayed in a browser. MarkupStructure Mark up the structure on the PDF pages so that it can be seen in a PDF reader. UpdateActualText The logical structure can contain a copy of text which is drawn on the page. Purge The tagged structure of the document references items displayed on the page. ReplaceImages Replace a set of images with a new one. ReplaceText Replace one item of text with another. &nbsp;

## Property Description Catalog The Catalog object at the root of the document. Root The StructureElement at the root of the tagging structure. ParentTree The ParentTree for the tagged structure.