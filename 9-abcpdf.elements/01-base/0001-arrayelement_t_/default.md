---
title: "default"
css: "abcpdf-docs.css"
---

# ArrayElement&lt;T&gt; Class

Class ArrayElement.

This class represents an array of typed Elements.

Since it is an array, the core Atom it is created from should be an ArrayAtom.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.ArrayElement ```

`Implements: IList, IList`

`Type T : The type of Element that this ArrayElement contains.`

## Method Description ArrayElement&lt;T&gt; Create a new ArrayElement. IndexOf Determines the index of a specific Element. &nbsp;Insert Inserts an Element into the array at the specified position. &nbsp;RemoveAt Removes the Element at the specified index. &nbsp;Add Add an Element to the end of the array. Clear Removes all Elements from the array. Contains Determines whether the array contains a specific Element. CopyTo Copies the Elements into an array. Remove Removes an Element from the array. GetEnumerator Returns an enumerator that iterates through the collection. inherited methods... &nbsp;

## Property Description ElementType The Type of elements within the Array. ElementsIndirect Whether elements within the Array are required to be indirect. Nullable Whether NullAtom values are acceptable within the array. &nbsp;Item[int index] Gets or sets the Element at the specified index. Count Gets the number of Elements contained in the array. inherited properties...