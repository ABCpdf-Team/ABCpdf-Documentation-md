---
title: "09-todoublearray"
css: "abcpdf-docs.css"
---

# ToDoubleArray Function

Attempts to convert an ArrayAtom into an array of doubles, resolving any references as necessary.

## Syntax

**[C#]**

```csharp
virtual double[] ToDoubleArray(Atom atom, double def)
```

<span class=language>[Visual Basic]</span>  

            `Overridable Function ToDoubleArray(atom As Atom, def As double) As Double[]`
			
## Params

| Name | Description | 
| --- | --- |
| atom | The ArrayAtom from which to obtain the values. | 
| def | A default value for any entries which could not be converted to the correct type. | 
| return | The array. | 

## Notes

Attempts to convert an ArrayAtom into an array of doubles, resolving any references as necessary.

If the atom does not resolve to an ArrayAtom, then the return value will be null.

## Example

None.