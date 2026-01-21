---
title: "arrayatoms"
css: "abcpdf-docs.css"
---

# ArrayAtoms Property

| Type | Default Value | Read Only | Description | 
| --- | --- | --- | --- |
| **[C#]** ```csharp IDictionaryIndirectObject, ArrayAtom> ``` [Visual Basic] `IDictionaryIndirectObject, ArrayAtom>` | An IDictionary. | Yes | The content streams for the items that have been found. | 

## Notes

The content streams for the items that have been found.

These are stored as a dictionary mapping the owning object with the content stream.

The content stream itself is represented as a series of graphics operators converted using the [ArrayAtom.FromContentStream](../../../7-abcpdf.atoms/arrayatom/1-methods/fromcontentstream.md) method.

## Example

None.