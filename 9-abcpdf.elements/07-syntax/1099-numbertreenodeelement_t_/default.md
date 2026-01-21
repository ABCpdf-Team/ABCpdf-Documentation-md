# NumberTreeNodeElement&lt;T&gt; Class

This class represents a number tree node.

A number tree is a way of representing a mapping from integers to other Elements.

The standard PDF dictionary object does something similar, but it works natively in terms of strings rather than numbers and the PDF specification implies that it might not have been optimized for large numbers of items.

As such the PDF specification uses this type of tree structure, in areas where there may be large numbers of keys and values.

This class is always an indirect object because EntryKids requires it to be so.

This is definitively detailed in:.

[The ISO PDF Specification, ISO 32000-1:2008 PDF 1.7; Table: 37, page 91.](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf#page=99)

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.TreeNodeElement WebSupergoo.ABCpdf13.Elements.NumberTreeNodeElement ```

## Method Description NumberTreeNodeElement&lt;T&gt; Create a new NumberTreeNodeElement. inherited methods... &nbsp;

## Property Description EntryKids This property represents the "Kids" entry of the number tree node dictionary object. EntryNums This property represents the "Nums" entry of the number tree node dictionary object. EntryLimits This property represents the "Limits" entry of the number tree node dictionary object. inherited properties...