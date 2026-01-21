# ObjectSoupSubset Class

A set of [IndirectObjects](../1-indirectobject/default.md) from an [ObjectSoup](../2-objectsoup/default.md).

This may be used for selecting related objects and copying them to a new soup while maintaining the relationships between the items in the selection.

``` System.Object WebSupergoo.ABCpdf13.Objects.ObjectSoupSubset ```

## Method Description ObjectSoupSubset Construct an ObjectSoupSubset. CopyTo Copy the objects in this subset to a new soup while preserving the relationships between the items in the selection. &nbsp;AddFamily Add a parent object along with all objects it refers to. &nbsp;AddOnlyOne Add just this object ignoring any objects it may refer to. &nbsp;

## Property Description Objects The collection of IndirectObjects currently contained in the subset. RemapIDs Gets the dictionary used to map object IDs from the source soup to new object IDs in the final soup. RemapTypes A dictionary used to redirect all objects of a specific type to a specific object ID.