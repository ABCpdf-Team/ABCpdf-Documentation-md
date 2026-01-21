---
title: "2-copyto"
css: "abcpdf-docs.css"
---

# CopyTo Function

Copies the items into a collection.

## Syntax

**[C#]**

```csharp
void CopyTo(Field[] array, int index)
```

<span class=language>[Visual
            Basic]</span>  
`Sub CopyTo(array As Field(), index As Integer)`
## Params

| Name | Description | 
| --- | --- |
| array | The array that is the destination for the elements. | 
| index | The zero-based index in array at which copying begins. | 

## Notes

Copies the elements of the collection to an array starting at a particular array index.

The array must be one-dimensional and have zero-based indexing.

## Example

None.