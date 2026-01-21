---
title: "fromxtransform"
css: "abcpdf-docs.css"
---

# FromXTransform Function

Create an ArrayAtom from a XTransform representation

## Syntax

**[C#]**

```csharp
static ArrayAtom FromXTransform(XTransform value)
```

<span class=language>[Visual
            Basic]</span>  

            `Shared Function FromXTransform(value As XTransform) As ArrayAtom`
## Params

| Name | Description | 
| --- | --- |
| value | The XTransform representing the value of the object. | 

## Notes

Create an ArrayAtom from a XTransform representation.

The ArrayAtom will contain six [NumAtoms](../../numatom/default.md) corresponding to the elements of the transform.

## Example

None.