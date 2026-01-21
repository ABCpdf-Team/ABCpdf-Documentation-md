---
title: "default"
css: "abcpdf-docs.css"
---

# TreeNodeElement Class

This class represents a name or number tree node dictionary.

This class is always an indirect object because CollectionElement.EntryResources, NameTreeNodeElement.EntryKids, NumberTreeNodeElement.EntryKids, NavigatorElement.EntryResources and NavigatorElement.EntryStrings require it to be so.

This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 36, page 89.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=97)

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.TreeNodeElement WebSupergoo.ABCpdf13.Elements.NameTreeNodeElement WebSupergoo.ABCpdf13.Elements.NumberTreeNodeElement ```

## Method Description TreeNodeElement Create a new TreeNodeElement. inherited methods... &nbsp;

## Property Description IsRoot Nodes in a tree may be root, intermediate or leaf. IsIntermediate Nodes in a tree may be root, intermediate or leaf. IsLeaf Nodes in a tree may be root, intermediate or leaf. inherited properties...