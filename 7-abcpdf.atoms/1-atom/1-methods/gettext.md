---
title: "gettext"
css: "abcpdf-docs.css"
---

# GetText Function

Gets the Text value from the Atom if it is a StringAtom.

## Syntax

**[C#]**

```csharp
static string GetText(Atom atom)
```

**[Visual Basic]**

`Shared Function GetText(atom As Atom) As String`
## Params

| Name | Description | 
| --- | --- |
| atom | The Atom to get the text from. | 
| return | The returned text. | 

## Notes

Get the Text value from the supplied Atom if it is a StringAtom.

If the atom is not a StringAtom or if it is null then an empty string ("") will be returned.

## Example

None.