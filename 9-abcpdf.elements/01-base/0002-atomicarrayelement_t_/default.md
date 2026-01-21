# AtomicArrayElement&lt;T&gt; Class

Class AtomicArrayElement.

This class represents an array of atomic elements.

By atomic, we mean elements that can be directly represented using a .NET equivalent such as a string or int.

On the PDF side the elements that are acceptable may be types such as StringAtom or NameAtom.

The set of acceptable types may be indicated using the AtomicTypes property.

Since it is an array, the core Atom this class is created from should be an ArrayAtom.

``` System.Object WebSupergoo.ABCpdf13.Elements.Element WebSupergoo.ABCpdf13.Elements.AtomicArrayElement ```

`Implements: IList, IList`

`Type T : Can be string, int, double, double? or bool.`

## Method Description &nbsp;AtomicArrayElement&lt;T&gt; Create a new AtomicArrayElement. IndexOf Determines the first index matching a specific value. &nbsp;Insert Inserts an item into the array at the specified position. &nbsp;RemoveAt Removes the item at the specified index. Add Add an item to the end of the array. Clear Removes all items from the array. Contains Determines whether the array contains a specific value. CopyTo Copies the items into an array. Remove Removes the first matching value from the array. GetEnumerator Returns an enumerator that iterates through the collection. inherited methods... &nbsp;

## Property Description AtomicTypes The Type of elements within the Array. &nbsp;Item[int index] Gets or sets the items at the specified index. Count Gets the number of items contained in the array. inherited properties...