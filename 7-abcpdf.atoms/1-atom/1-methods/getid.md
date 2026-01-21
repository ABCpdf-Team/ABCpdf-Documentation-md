---
title: "getid"
css: "abcpdf-docs.css"
---

# GetID Function

Gets the Object ID value from the Atom if it is a RefAtom.

## Syntax

**[C#]**

```csharp
static int GetID(Atom atom)
```

**[Visual Basic]**

`Shared Function GetID(atom As Atom) As Integer`
## Params

| Name | Description | 
| --- | --- |
| atom | The Atom to get the Object ID from. | 
| return | The returned Object ID. | 

## Notes

Get the Object ID from the supplied Atom if it is a RefAtom.

If the atom is not a RefAtom or if it is null then zero will be returned.

## Example

None.