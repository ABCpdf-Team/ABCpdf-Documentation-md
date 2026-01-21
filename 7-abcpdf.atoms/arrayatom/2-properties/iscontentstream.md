---
title: "iscontentstream"
css: "abcpdf-docs.css"
---

# IsContentStream Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp bool ``` [Visual Basic] `Boolean` | false | No | Determines whether the ArrayAtom represents a content stream or not. | 

## Notes

Determines whether the [ArrayAtom](../default.md) represents a content stream or not.

[ArrayAtoms](../default.md) do not normally contain streams or operators. To allow them to do this you need to set this property to true.

In most situations ABCpdf will parse the content stream for you and set the property appropriately.

However if you creating your own streams you may need to specify that the array needs to support these types of atoms.

## Example

None.