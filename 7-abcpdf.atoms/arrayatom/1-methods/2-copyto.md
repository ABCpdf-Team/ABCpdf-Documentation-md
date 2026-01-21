---
title: "2-copyto"
css: "abcpdf-docs.css"
---

# CopyTo Function

Copies the Atoms into an array.

## Syntax

**[C#]**

```csharp
void CopyTo(Atom[] array, int index)
```

<span class=language>[Visual
            Basic]</span>  
`Sub CopyTo(array As Atom(), index As Integer)`
## Params

| Name | Description | 
| --- | --- |
| array | The array that is the destination for the elements. | 
| index | The zero-based index in array at which copying begins. | 

## Notes

Copies the elements of the Collection to an array starting at a particular array index.

The array must be one-dimensional and have zero-based indexing.

## Example

None.