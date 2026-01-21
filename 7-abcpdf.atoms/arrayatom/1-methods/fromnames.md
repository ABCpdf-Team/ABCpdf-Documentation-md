---
title: "fromnames"
css: "abcpdf-docs.css"
---

# FromNames Function

Create an ArrayAtom of NameAtoms from a list of strings.

## Syntax

**[C#]**

```csharp
static ArrayAtom FromNames(IList items)
```

<span class=language>[Visual
            Basic]</span>  

            `Shared Function FromNames(items as IList(Of String)) As ArrayAtom`
## Params

| Name | Description | 
| --- | --- |
| items | The list of strings. | 
| return | The resulting ArrayAtom. | 

## Notes

Create an ArrayAtom of NameAtoms from a list of strings.

If the provided list is null then the return value will be null.

## Example

None.