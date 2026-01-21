---
title: "removeitem"
css: "abcpdf-docs.css"
---

# RemoveItem Function

Removes the named entry from the Atom if it is a DictAtom.

## Syntax

**[C#]**

```csharp
static void RemoveItem(Atom atom, string key)
```

**[Visual Basic]**

`Shared Sub RemoveItem(atom As Atom, key As String)`
## Params

| Name | Description | 
| --- | --- |
| atom | The Atom from which the item should be removed. | 
| key | The name of the item to be removed. | 

## Notes

[DictAtoms](../../dictatom/default.md) can contain other Atoms referenced by name.

This function allows you to remove a named item from a DictAtom.

If the atom supplied is not a DictAtom then calling this function will have no effect.

## Example

None.