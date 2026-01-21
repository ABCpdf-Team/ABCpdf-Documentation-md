---
title: "8-remove"
css: "abcpdf-docs.css"
---

# Remove Function

Removes an Atom from the array.

## Syntax

**[C#]**

```csharp
bool Remove(Atom value)
```

**[Visual Basic]**

`Function Remove(value As Atom) As Boolean`
## Params

| Name | Description | 
| --- | --- |
| value | The Atom to be removed. | 
| return | True if the Atom is removed, otherwise false. | 

## Notes

When an Atom is removed the elements that follow the removed element move up to occupy the vacated spot.

## Example

None.