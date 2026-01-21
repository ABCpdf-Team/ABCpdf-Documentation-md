---
title: "10-tostringarray"
css: "abcpdf-docs.css"
---

# ToStringArray Function

Attempts to convert an ArrayAtom into an array of strings, resolving any references as necessary.

## Syntax

**[C#]**

```csharp
virtual string[] ToStringArray(Atom atom)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ToStringArray(atom As Atom) As string[]`
			
## Params

| Name | Description | 
| --- | --- |
| atom | The ArrayAtom from which to obtain the values. | 
| return | The array. | 

## Notes

Attempts to convert an ArrayAtom into an array of strings, resolving any references as necessary.

If the atom does not resolve to an ArrayAtom, then the return value will be null.

Any entries which could not be coverted to the correct type will be null.

## Example

None.