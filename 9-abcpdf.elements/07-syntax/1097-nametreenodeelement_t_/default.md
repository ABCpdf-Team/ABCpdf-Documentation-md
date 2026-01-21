# NameTreeNodeElement&lt;T&gt; Class

This class represents a name tree node.

A name tree is a way of representing a mapping from strings to other Elements.

The standard PDF dictionary object does something similar, but it works natively in terms of shorter, non-Unicode strings and the PDF specification implies that it might not have been well optimized for large numbers of items.

As such the PDF specification uses this type of tree structure, in areas where there may be large numbers of keys and values.

This class is always an indirect object because CollectionElement.EntryResources, EntryKids, NavigatorElement.EntryResources and NavigatorElement.EntryStrings require it to be so.

This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 36, page 89.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=97)

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.TreeNodeElement WebSupergoo.ABCpdf13.Elements.NameTreeNodeElement ```

## Method Description NameTreeNodeElement&lt;T&gt; Create a new NameTreeNodeElement. inherited methods... &nbsp;

## Property Description EntryKids This property represents the "Kids" entry of the name tree node dictionary object. EntryNames This property represents the "Names" entry of the name tree node dictionary object. EntryLimits This property represents the "Limits" entry of the name tree node dictionary object. inherited properties...