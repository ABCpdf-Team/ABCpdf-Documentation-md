---
title: "5-fromatom"
css: "abcpdf-docs.css"
---

# FromAtom Function

Create an XRect from a standard PDF Rectangle ArrayAtom.

## Syntax

**[C#]**

```csharp
static XRect FromAtom(IndirectObject io, ArrayAtom array)
```

<span class=language>[Visual Basic]</span>  

              `Shared Function FromAtom(io As IndirectObject, array As ArrayAtom) As XRect`
## Params

| Name | Description | 
| --- | --- |
| io | Any IndirectObject from the document. | 
| array | An ArrayAtom containing four NumAtoms. | 
| return | The newly created XRect object. | 

## Notes

Create an XRect from a standard PDF Rectangle ArrayAtom.

Such arrays typically contain four numbers - lower left x and y coordinates followed by upper right x and y.

However this is a convention and any two diagonally opposite points are acceptable.

If the array is null or the entries do not resolve to four NumAtoms then the return value will be null.

## Example

None.