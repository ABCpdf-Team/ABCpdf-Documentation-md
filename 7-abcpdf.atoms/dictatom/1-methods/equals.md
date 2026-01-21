---
title: "equals"
css: "abcpdf-docs.css"
---

# Equals Function

Test whether the two DictAtoms are the same

## Syntax

**[C#]**

```csharp
bool Equals(DictAtom other)
```

<span class=language>[Visual
            Basic]</span>  

            `Function Equals(other As DictAtom) As Boolean`
## Params

| Name | Description | 
| --- | --- |
| other | The DictAtom to test against. | 

## Notes

Test whether the two DictAtoms are the same.

Two DictAtoms are judged to be equal if they have the same named entries and the Atom corresponding with each named entry is equal to the corresponding Atom in the other dictionary.

## Example

None.