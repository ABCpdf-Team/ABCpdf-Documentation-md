---
title: "02-addstructparents"
css: "abcpdf-docs.css"
---

# AddStructParents Function

Add a new StructParents to the tree.

## Syntax

**[C#]**

```csharp
int AddStructParents(IndirectObject io, bool commit)
```

<span class=language>[Visual Basic]</span>  

            `Sub AddStructParents(io As IndirectObject, commit As bool) As Integer`
			
## Params

| Name | Description | 
| --- | --- |
| io | The object to be added. | 
| commit | Whether to commit changes to the document. | 
| return | The logical structure key for this object. | 

## Notes

Add a new StructParents to the tree.

Items are held in a cache and are not pushed through to the document until committed.

## Example

None.