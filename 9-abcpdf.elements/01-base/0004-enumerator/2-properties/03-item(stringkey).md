---
title: "03-item(stringkey)"
css: "abcpdf-docs.css"
---

# Item(string key) Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp T ``` [Visual Basic] `T` | null | No | Gets or sets the Element at the specified index. | 

`KeyNotFoundException: Thrown if getting an item, but the specified key was not found. NullReferenceException: Thrown if an attempt is made to assign a null value.`

## Notes

Gets or sets the [Element](../../1086-element/default.md) at the specified index. In C# this property is the indexer for the class.

The Item property is used to access [Elements](../../1086-element/default.md) within the dictionary.

The DictAtom is accessed and used to create an [Element](../../1086-element/default.md) of type T.

In the case that T has multiple sub-types, default factories will result in an item of the correct subtype being created.

The precise factory that should be used is determined at the point the [DictElement](../../0003-dictelement_t_/default.md) is assigned to a property of another [Element](../../1086-element/default.md).

So since different properties may use different factories, you should not share one [DictElement](../../0003-dictelement_t_/default.md) between more than one property.

[DictElements](../../0003-dictelement_t_/default.md) cannot hold null values in a meaningful way. So if you provide a null value, this will result in an exception being raised.

If the specified key is not found, a get operation throws a KeyNotFoundException, and a set operation creates a new element with the specified key.

## Example

None.